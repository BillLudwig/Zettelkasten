title:: Conditionally Adaptive CSS. Browser Behavior That Might Improve Your Performance — Vadim Makeev by pepelsbey.dev
author:: [[pepelsbey.dev]]
full-title:: "Conditionally Adaptive CSS. Browser Behavior That Might Improve Your Performance — Vadim Makeev"
category:: #articles
url:: https://pepelsbey.dev/articles/conditionally-adaptive/

- [[Highlights]] first synced by [[Readwise]] [[November 15th, 2022]]
	- What if we’d take the CSS bundle we’ve just built out of dozens of files and split it back into multiple parts? But this time, based on conditions where these parts are applicable. For example, we could split it into four files:Base: universal styles with fonts and colorsMobile: styles only for narrow viewportsTablet: styles only for medium viewportsDesktop: styles only for large viewports
	- <link    rel="stylesheet" href="base.css"><link    rel="stylesheet" href="mobile.css"    media="(max-width: 767px)"><link    rel="stylesheet" href="tablet.css"    media="(min-width: 768px) and (max-width: 1023px)"><link    rel="stylesheet" href="desktop.css"    media="(min-width: 1024px)">
	- Browsers are smart enough not to prioritize resources that aren’t relevant to the current media conditions.
	- The list of media features you can use in Media Queries extends beyond just viewport width and height. You can adapt your website to the user’s needs and preferences: color scheme, pixel density, reduced motion, etc. But not only that! With this new behavior in mind, we can make sure that only relevant styles are render-blocking.
	- Safari doesn’t support this behavior