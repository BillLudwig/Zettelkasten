- ## Media Queries
	- [Personalize It!](https://css-tricks.com/personalize-it/) Using preference-query [[Dev/Web/CSS]] for [[Dev/A11y]] by Una Kravets
	  id:: 6377c180-d2eb-437a-919d-fd2a58ce8c02
- ## Tips and Tricks
	- [Style a parent element based on its number of children using CSS :has()](https://www.bram.us/2022/11/17/style-a-parent-element-based-on-its-number-of-children-using-css-has)
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
	- [[Using Picture And Source Tags To Prevent Loading Hero Image On Mobile Devices]] #Dev/Web/CSS
	  id:: 641a4e8a-d968-4070-9010-037ef3d67753
- ## References
	- [What CSS Do You Absolutely Have to Know in 2022](https://css-tricks.com/what-css-do-you-absolutely-have-to-know-in-2022/) by Geoff Graham #[[November 8th, 2022]]
	- [Practical CSS Guide for Busy Developers](https://codefrontend.com/css-guide/) by Vincas Stonys #[[October 28th, 2022]]
	- [Keeping Your CSS Small: scopes, containers, and other new stuff](https://www.youtube.com/watch?v=bz0sMsCiU1c) [[Dev/Web/CSS]] [[Video]] by Tab Atkins-Bittner Sept, 9 2022
	  id:: 6373dc00-ac71-44a7-818f-015a3a05f561
	- [The evolution of scalable CSS](https://frontendmastery.com/posts/the-evolution-of-scalable-css/): A deep dive into the problems with scaling CSS on large projects. Understand the evolution of CSS best practices. #[[November 12th, 2022]]
	  id:: 6377ab8f-e56d-4bf1-a484-1df9a3d7791c
	- [What should someone learn if they last boned up during CSS3](https://css-tricks.com/whats-new-since-css3/) by Chris Coyier. #[[August 25th, 2022]]
	  id:: 6377be6b-89e0-4885-933a-9b418e9824aa