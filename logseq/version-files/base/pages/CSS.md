tags:: WebDev

- ## Reference Videos
- ## Media Queries
	- [Personalize It!](https://css-tricks.com/personalize-it/) Using preference-query [[CSS]] for [[A11y]] by Una Kravets
- ## Tips and Tricks
	- [Style a parent element based on its number of children using CSS `:has()`](https://www.bram.us/2022/11/17/style-a-parent-element-based-on-its-number-of-children-using-css-has)
	  id:: 637963df-b27f-4cd6-adcc-7312ed841ca2
	  collapsed:: true
		- > /* At most 3 (3 or less, excluding 0) children */
		  ul:has(> :nth-child(-n+3):last-child) {
		  	outline: 1px solid red;
		  }
		  /* At most 3 (3 or less, including 0) children */
		  ul:not(:has(> :nth-child(3))) {
		  	outline: 1px solid red;
		  }
		  /* Exactly 5 children */
		  ul:has(> :nth-child(5):last-child) {
		  	outline: 1px solid blue;
		  }
		  /* At least 10 (10 or more) children */
		  ul:has(> :nth-child(10)) {
		  	outline: 1px solid green;
		  }
		  /* Between 7 and 9 children (boundaries inclusive) */
		  ul:has(> :nth-child(7)):has(> :nth-child(-n+9):last-child) {
		  	outline: 1px solid yellow;
		  }
	- [Collapsible Tree Lists with CSS](https://iamkate.com/code/tree-views/) - No Javascript and fully accessible.
	- You can style the button portion of input[type=file] with `::file-selector-button`
	- [[Using Picture And Source Tags To Prevent Loading Hero Image On Mobile Devices]] #CSS
	  id:: 641a4e8a-d968-4070-9010-037ef3d67753
	- [Prevent Transitions as a Page is Loading](https://chriscoyier.net/2023/04/05/prevent-transitions-as-a-page-is-loading/) #CSS
	  id:: 642e31ea-abb1-4bb0-afc9-154b63cf0d08
		- ```
		  <body class="preload">
		  
		  window.addEventListener("load", () => {
		    document.body.classList.remove("preload");
		  });
		  
		  .preload * { 
		    transition: none !important;
		    animation-duration: 0.001s !important; 
		  }
		  ```
	- ### Visibility
		- `: hidden` - Keeps height and width
		- `: none` - Hides everything within a container
		- use `content-visibility: hidden` to hide the contents of a container without keeping their height and width
	- ### Responsive Text
		- [Responsive fluid CSS type scales](https://tobiasahlin.com/blog/responsive-fluid-css-type-scales/) - I love responsive font scales and this looks about as perfect as we can get right now. It's too bad it's in `px` but that is a temporary problem. #CSS
		  id:: 651e116e-7bc0-4b0b-a619-d0f57a74b339
			- ```
			  :root {
			    --min-size: 12;
			    --max-size: 18;
			    --container-min: 320;
			    --container-max: 2400;
			  }
			  
			  /* Setup size calculation for all max utilities */
			  .h1-max, .h2-max, .h3-max, .h4-max, .h5-max, .h6-max, .h7-max, .h8-max {
			    --font-size: calc(var(--min-size) * 1px + (var(--max-size) - var(--min-size)) * (100cqw - var(--container-min) * 1px) / (var(--container-max) - var(--container-min)));
			    font-size: clamp(var(--min-size) * 1px, var(--font-size), var(--max-size) * 1px);
			  }
			  
			  .h1-max { --max-size: 128; }
			  .h2-max { --max-size: 96; }
			  .h3-max { --max-size: 64; }
			  .h4-max { --max-size: 48; }
			  .h5-max { --max-size: 32; }
			  .h6-max { --max-size: 24; }
			  .h7-max { --max-size: 16; }
			  .h8-max { --max-size: 12; }
			  
			  .h1-min { --min-size: 128; }
			  .h2-min { --min-size: 96; }
			  .h3-min { --min-size: 64; }
			  .h4-min { --min-size: 48; }
			  .h5-min { --min-size: 32; }
			  .h6-min { --min-size: 24; }
			  .h7-min { --min-size: 16; }
			  .h8-min { --min-size: 12; }
			  ```
- ## References
	- [What CSS Do You Absolutely Have to Know in 2022](https://css-tricks.com/what-css-do-you-absolutely-have-to-know-in-2022/) by Geoff Graham #[[November 8th, 2022]]
	- [Practical CSS Guide for Busy Developers](https://codefrontend.com/css-guide/) by Vincas Stonys #[[October 28th, 2022]]
	- [Keeping Your CSS Small: scopes, containers, and other new stuff](https://www.youtube.com/watch?v=bz0sMsCiU1c) [[CSS]] [[Video]] by Tab Atkins-Bittner Sept, 9 2022
	  id:: 6373dc00-ac71-44a7-818f-015a3a05f561
	- [The evolution of scalable CSS](https://frontendmastery.com/posts/the-evolution-of-scalable-css/): A deep dive into the problems with scaling CSS on large projects. Understand the evolution of CSS best practices. #[[November 12th, 2022]]
	  id:: 6377ab8f-e56d-4bf1-a484-1df9a3d7791c
	- [What should someone learn if they last boned up during CSS3](https://css-tricks.com/whats-new-since-css3/) by Chris Coyier. #[[August 25th, 2022]]
	  id:: 6377be6b-89e0-4885-933a-9b418e9824aa