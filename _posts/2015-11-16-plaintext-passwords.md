---
layout:     post
title:      "Share you wifi passwords easily with MyFi"
subtitle:   "...because it's stored in plaintext on your phone"
date:       2015-11-16 17:08:00
author:     "Sriram"
header-img: "img/post-bg-01.jpg"
---

The Android OS uses a 'mini' version of `wpa_supplicant`[^ws] for managing WiFi connnections and the configuration details for every WiFi connnection on your phone/tablet is stored in a plaintext configuration file. This is not really an issue for most people since the devices are usually unrooted and hopefully they have the sense not to reuse their social network passwords as their wifi passwords. At PhoneLab[^pl], we generally work with rooted phones in lab and if you want to login to the university wifi, you need to use your university login to authenticate yourself. A malicious application can use this to gather login information for these accounts. Anyone having a rooted device and using similar methods to connect to wifi are at risk of having their login information stolen. Granted the chances of this happening is very small but it's a vulnerability nonetheless.

But this does help you share you wifi logins easily with others. The MyFi app reads the passwords currently stored on the device and lets you share it with your friends through NFC. All you have to do is select the wifi network and tap your friend's device.

Get the app here,
[MyFi](https://play.google.com/store/apps/details?id=io.github.srirambms.myfi)


[^ws]:[wpa_supplicant :](https://en.wikipedia.org/wiki/Wpa_supplicant)
[^pl]:[PhoneLab :](https://phone-lab.org/)
