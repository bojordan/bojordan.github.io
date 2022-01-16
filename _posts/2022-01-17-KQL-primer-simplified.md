---
layout: post
title: KQL primer, simplified
---

### A good official tutorial exists

As prep for a learning presentation at work, I set out to turn a quick set of “primer” notes into a more thought-out blog post, and then hopefully a better presentation. Turns out, I quickly found a far better introduction to the language. This [docs.microsoft.com tutorial](https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/tutorial?pivots=azuredataexplorer) is wonderful; it is simple and straightforward, and I used it for my talk.

### Learning how to dig

So, rather than specifically a technical introduction, what is it that I am trying to share about KQL? Kusto is such an amazingly performant system, that using it can actually be fun.

Wait - poring through telemetry can be fun?

What I want to convey in 15 minutes or less is how to discover what data you have, and how to conveniently dig. I have met a lot of engineers whose systems publish to a KQL system. They've had access to the data for years, and don’t know how to discover what’s there.

The noise of that sea of poorly conceived and messy telemetry can be intimidating. Don’t let it be.

So, my old KQL primer has become the following "things to learn". When I share these, I always hope it sparks a little curiosity. That's all.

Learn the following concepts, as quickly as possible.

1. Browse tables, looking at a few random records.

   ```
   traces | take 10
   ```

   Perhaps union all your tables together:

   ```
   union traces, exceptions, ... |
   ```

2. Filter on timestamps. Most KQL UIs will allow you to paste the text of a timestamp and it will wrap it in a ```datetime()``` declaration.

    ```
    | where timestamp > ago(1d)
    | where timestamp > [PASTE TIME] and timestamp < [PASTE TIME]```
    | where timestamp between (datetime(2022-01-12 19:54:00) .. datetime(2022-01-12 20:10:54)))
    ```

3. Search for strings. Get hooked on Kusto's amazing indexing.

    ```
    // no substring matches
	StormEvents
	| where * has "caro"

    // includes substring matches
	StormEvents
	| where * contains "caro"
    ```

4. Create your own columns, on the fly. Compute new values, or pull data from a column with a complex data object out to its own column.

    ```
    StormEvents
    | extend Duration = EndTime - StartTime

    Covid19_Bing
    | where Id == "/US/North Carolina"
    | extend ConfirmedValue = Confirmed.Value,
        ActiveValue = Active.Value,
        DeathsValue = Deaths.Value,
        RecoveredValue = Recovered.Value

    ```

5. Remove columns you don't need.

    ```
    | project Id, ReportDate, ConfirmedValue, ActiveValue, DeathsValue, RecoveredValue
    ```

6. Group results and run functions over the set

    ```
    Covid19_Bing
    | where Id == "/US/North Carolina"
    | extend ConfirmedValue = Confirmed.Value, ActiveValue = toint(Active.Value), DeathsValue = Deaths.Value, RecoveredValue = Recovered.Value
    | project Id, ReportDate, ConfirmedValue, ActiveValue, DeathsValue, RecoveredValue
    | summarize count(), toint(avg(ActiveValue)) by bin(ReportDate, 31d)
    ```

7. Get values out of JSON columns

8. Join against other records.

 Note, I'm assuming most queries will be using the sample data from the tutorial listed above, but my one criticism of the data from that tutorial is that it is not typical system telemetry.
 I'll describe this later

