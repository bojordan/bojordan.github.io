---
layout: post
title: iPhone 14 Pro Max
---

This is my year for an iPhone update, and I received the new phone yesterday. Upgrading from my iPhone 12 Pro Max was more straightforward than I feared, and definitely more seamless than last time. I used [Quick Start](https://support.apple.com/guide/iphone/turn-on-and-set-up-iphone-iph1fd7e482f/ios) to transfer, and things worked as expected... mostly.
<!--more-->
My service is with Verizon, and the new iPhone was purchased without any carrier affiliation. I was using the standard old-fashined SIM in the iPhone 12 Pro Max.

1. Right before starting the process, I did a fresh iCloud back-up.
1. I started up the new phone and selected Quick Start.
1. I chose the direct transfer between devices. This did not take nearly as long as the warned estimation time.
1. I followed the prompts and most things transferred seamlessly. I did not select carrier activation during this parocess.
1. It provided me the option of transferring over my Apple Watch connection. I left the selection as-is. I did not unpair from the old phone or anything unintuitive as was required in the past.
1. I use Microsoft Authenticator. My accounts did not transfer, but I realized I was not using iCloud back-up for Authenticator. I turned this on in the app on the old phone, and got the accounts to show up on the new one. However, for most of the identities I had registered, I had to re-estabilish the device to MFA for them. For Microsoft identities, this involved visiting https://mysignins.microsoft.com/security-info for each and generating the QR code dance.
1. I also had to re-establish corporate management of my device, which involves Microsoft Intune and Defender installation. Attempting to re-enter the password to corporate email account is one way to make sure this is all getting kicked off.
1. I had to restablish my Testflights by launching the Testflight app and re-installing. They did not find their way back to their locations in Springboard.
1. Developer profile policies had to re-downloaded and re-trusted.
1. Finally, I wanted to transfer the number to the new phone, which involves eSIM, now. This involved going to the Verizon portal and going through their "activate your own phone on an existing number" flow. In Verizon's the instructions it led me to enter the id of the new phone's second IMEI (which is apparently the second SIM identifier - "IMEI2" - in the Settings -> General -> About). Note, their documentation says the first IMEI is for an inserted SIM card. iPhone 14 Pro only has eSIM, but it shows IMEI and IMEI2; I provided IMEI2 to Verizon and got a green checkbox.
1. I confirmed the transfer on the Verizon site, and it sat for a minute and eventually failed with an error saying to call their support line. It had at least half-way worked, however, as my old phone no longer got cellular singal. However, the new phone didn't work, so I started the support call on another phone (oops).
1. While waiting, I poked on the new phone, and eventually saw a top-level prompt in Settings that there was an activating step waiting. I noticed this as an operator was finally coming on the line; I pressed the confirm button in Settings, and the phone went live almost immediately. The support person had me perform a test call, but all was fine.

When reading this it may sound like a lot, but this entire process took probably 2 hours.