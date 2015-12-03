---
layout:     post
title:      "Flashing a custom Android kernel"
subtitle:   "It's not as difficult as the Internet makes it seem"
date:       2014-08-26 12:00:00
author:     "Sriram"
description: "It's not as difficult as the Internet makes it seem"
tags: [kernel, bootloader, adb, android]
categories: [android, development]
header-img: "img/post-bg-01.jpg"
---

<p>
	I had a really hard time figuring out how to flash a custom kernel on my Android phone for one of my projects. Since I was pressed for time, I didn't have the luxury of following some of the really long guides on the Internet to get this working. And turns out, you don't have to. Once you have your kernel compiled and ready, and I'm assuming you know how to do that, all you have to do to flash it to the phone is to put the phone in fastboot mode,
</p>
`adb reboot bootloader`

<p>
	And then you simply flash the zImage to the phone with the following command.
</p>
`fastboot flash zimage <path to compiled zImage file>`

<p> And you're done.</p>
