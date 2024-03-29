tags:: CSS

- ## Snippets
	- Baseline for default links [^1]
		- ```
		  /* Baseline for default links */
		  a:not([class]) {
		    /* Relatively sized thickness and offset */
		    text-decoration-thickness: max(0.08em, 1px);
		    text-underline-offset: 0.15em;
		  }	
		  ```
	- Focus-visible styling [^1]
		- ```
		  :focus-visible {
		    --outline-size: max(2px, 0.15em);
		  
		    outline: var(--outline-width, var(--outline-size)) var(--outline-style, solid)
		      var(--outline-color, currentColor);
		    outline-offset: var(--outline-offset, var(--outline-size));
		  }
		  ```
	- Scroll padding to put space between top/bottom of viewport and anchor target (this doesn't work without JavaScript if you have sticky headers or footers) [^1]
		- ```
		  /* Scroll padding allowance above anchor links */
		  :target {
		    scroll-padding-block-start: 2rem;
		  }
		  ```
		- ```
		  /* Scroll padding allowance below focused elements to ensure they are clearly in view */
		  :focus {
		    scroll-padding-block-end: 8vh;
		  }
		  ```
	- Apply smooth scrolling when user hasn't set motion preference to "reduce"
		- ```
		  @media (prefers-reduced-motion: no-preference) {
		    html {
		      scroll-behavior: smooth;
		    }
		  }
		  ```
- ## Resources
	- ~~[My Custom CSS Reset](https://www.joshwcomeau.com/css/custom-css-reset/) by Josh Comeau~~
	- Andy Bell released a [(more) Modern CSS Reset](https://docs.google.com/document/d/1r07qSL2lhu36qILXzNIGr9D_m0GPqjsQub4lXl4CJG4/edit?usp=sharing) that I'll be using on all my new projects. #[[CSS Reset]]
	  id:: 651cc728-1ca7-4672-a236-805320b272cf
- Sources:
	- 1:: https://moderncss.dev/modern-css-for-dynamic-component-based-architecture
	  2:: https://css-irl.info/reducing-complexity-in-front-end-development