---
layout:     post
title:      "Accessibility Feature For The Color Blind"
subtitle:   ""
date:       2015-01-23 16:00:00
author:     "Sriram"
header-img: "img/post-bg-01.jpg"
---

This was my entry for the UB Hackathon. My idea was to add a new accessibility feature for the color blind. People who are color blind are unable to distinguish between two colors. The most common type is the inability to distinguish between green and red. My solution was to to simply replace the green with blue, which is a combination that they can distinguish.  

I used Jeff Sharkey's code [^code]  to manipulate the colors. It doesn't exactly swap the colors as I didn't have the time to play with openGL, so I just blended other colors to get the desired effect. People who are colorblind can use the Ishihara color test plate[^ishi] and go through the available modes and pick one that works for them. The settings are merged with the existing 'Accessibility' option. I reused the JNI interface I had written for a previous project for communicating the setting to the SurfaceFlinger module. I modified SurfaceFlinger to read the system properties updated through the JNI interface and use that value to apply the corresponding color scheme. It's not an efficient way to do this, since SurfaceFlinger ends up querying the system property everytime it draws on the screen but I didn't notice any lag or unresponsiveness due to these changes. The entire project was written over a period of two days and some of the color modes might not be usable at all as I didn't have any way to test it, but a proper implementation of this idea should first go through the 24 Ishihara plates to first determine the type of color blindness and then present a set of color options to choose from. 


<a href="/img/accessibility/accessibility1.png" data-lightbox="accessgallery" class="gallery-image-link"><img src="/img/accessibility/accessibility1.png" class="gallery-image"></a>
<a href="/img/accessibility/accessibility2.png" data-lightbox="accessgallery" class="gallery-image-link"><img src="/img/accessibility/accessibility2.png" class="gallery-image"></a>
<a href="/img/accessibility/accessibility3.png" data-lightbox="accessgallery" class="gallery-image-link"><img src="/img/accessibility/accessibility3.png" class="gallery-image"></a>
<a href="/img/accessibility/accessibility4.png" data-lightbox="accessgallery" class="gallery-image-link"><img src="/img/accessibility/accessibility4.png" class="gallery-image"></a>
<a href="/img/accessibility/accessibility5.png" data-lightbox="accessgallery" class="gallery-image-link"><img src="/img/accessibility/accessibility5.png" class="gallery-image"></a>



#### Code 
>[![Github](/img/logos/GitHub-Mark-64px.png)](https://github.com/SriramBms/accessibility-feature-colorblind) [Accessibility Feature For The Color Blind](https://github.com/SriramBms/accessibility-feature-colorblind)



[^ishi]:[Ishihara color test plate][1]
[^code]:[Android SurfaceFlinger tricks for fun and profit][2]
[2]:<http://jsharkey.org/blog/2010/07/01/android-surfaceflinger-tricks-for-fun-and-profit/>
[1]: <http://www.dfisica.ubi.pt/~hgil/p.v.2/Ishihara/Ishihara.24.Plate.TEST.Book.pdf> "Ishihara color test"


<script>
$(document).ready(function() {
	$(".fancybox").fancybox({
		openEffect	: 'none',
		closeEffect	: 'none'
	});
});
</script>
