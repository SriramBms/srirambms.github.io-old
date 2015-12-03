---
layout:     post
title:      "Signing an Android app for a custom Android build"
subtitle:   ""
date:       2014-08-06 19:48:00
author:     "Sriram"
header-img: "img/post-bg-01.jpg"
---

<p>
	If you want to sign your apps for a custom Android build, first find the keys you used to sign the build. They can be usually found in,
</p>
`<source directory>/build/target/product/security/`

<p>
	You will see a bunch of keys in the folder. Find the platform `pem` and `pk8` files and sign the app with the following command,
</p>
`java -jar <source dir>/prebuilts/sdk/tools/lib/signapk.jar <source dir>/build/target/product/security/platform.x509.pem <source dir>/build/target/product/security/platform.pk8 your-app.apk your-app-signed.apk`

