- Source: https://www.bennadel.com/blog/4360-using-picture-and-source-tags-to-prevent-loading-hero-image-on-mobile-devices.htm
- ```
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