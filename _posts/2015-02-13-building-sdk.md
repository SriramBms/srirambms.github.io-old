---
layout:     post
title:      "Building the Android sdk"
subtitle:   ""
date:       2015-02-13 22:18:00
author:     "Sriram"
header-img: "img/post-bg-01.jpg"
---

In the root folder,

`. build/envsetup.sh`<br>
`lunch sdk-eng ` <br>
`make sdk `



Once it's done, the sdk can be found in the `/out/host/linux-x86/sdk/` folder. The simplest way to use the new sdk, in case you've added a new API, is by adding the new `android.jar`to build path.  

##### NOTE
> And droid doc errors (Error 45) can be resolved by executing <br>
>`git revert 5f9922d7c3bce158e4c7a58929d4075e7c91e32e` in the `<src>/frameworks/base` folder [^err].

[^err]:[https://groups.google.com/forum/#!topic/android-building/fo--bOxDTPQ :](https://groups.google.com/forum/#!topic/android-building/fo--bOxDTPQ)


