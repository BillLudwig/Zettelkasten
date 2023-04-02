title:: Notes: Why You Should Never Use Px to Set Font-Size in CSS
author:: joshcollinsworth.com
full-title:: "Why You Should Never Use Px to Set Font-Size in CSS - Josh Collinsworth Blog"
url:: https://joshcollinsworth.com/blog/never-use-px-for-font-size

- [[Highlights]] first synced by [[Readwise]] [[November 16th, 2022]]
	- px is short for pixel…although it’s not literally a pixel most of the time anymore.
	- 1px is equal to whatever the browser is treating as a single pixel (even if it’s not literally a pixel on the hardware screen).
	- Em originally referred to the width of an “M” character, which is where the name came from. But it now refers to the current font size, rather than to the dimensions of a specific glyph.
	- 1rem is always equal to the browser’s font size—or, more accurately the font size of the html element.
	- em, on the other hand, is the font size of the current element.
	- px values do not scale up or down when the user changes their font size
	- em and rem values do adjust in proportion to font size
	- Since we know that px values won’t change when and if the user adjusts their font size, that means pixel units are actually a great choice for some aesthetic elements.
	- I would not use px anywhere, except for design elements I explicitly did not want to scale with font size.