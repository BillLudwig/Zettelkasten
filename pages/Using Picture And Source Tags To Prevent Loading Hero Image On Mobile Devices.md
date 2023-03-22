- Source: https://www.bennadel.com/blog/4360-using-picture-and-source-tags-to-prevent-loading-hero-image-on-mobile-devices.htm
- ```
  <!---
  	Attempt to start preloading the hero image ASAP; but, only if it will be
  	shown based on the media query (which must match the CSS media query as well).
  --->
  <link
  	rel="preload"
  	href="/images/header/photos/#photo.src#"
  	as="image"
  	media="(min-width: 1024px)"
  />
  
  <picture>
  	<!--- Note that this src and media query match the link-preload tag. --->
  	<source
  		srcset="/images/header/photos/#photo.src#"
  		media="(min-width: 1024px)"
  	/>
  	<img
  		fetchpriority="high"
  		loading="eager"
  		alt="#encodeForHtmlAttribute( photo.alt )#"
  	/>
  </picture>
  ```