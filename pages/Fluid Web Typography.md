tags:: CSS

-
- ## Basic Example: [^1]
	- ```
	  .container {
	    container-type: inline-size;
	  }
	  
	  .fluid-type {
	    font-size: clamp(1rem, 4cqi, 3rem);
	  }
	  ```
	- The .container wrapper is required to get the `cqi` unit to work on resize [^1]
- ## Better Example [^1]
	- ```
	  :root {
	    --h1-base: 1.75rem;
	    --h2-base: 1.5rem;
	    --h3-base: 1.35rem;
	    --h4-base: 1.15rem;
	  }
	  
	  h1,
	  .h1 {
	    --font-size-base: var(--h1-base);
	  }
	  
	  h2,
	  .h2 {
	    --font-size-base: var(--h2-base);
	  }
	  
	  h3,
	  .h3 {
	    --font-size-base: var(--h3-base);
	  }
	  
	  h4,
	  .h4 {
	    --font-size-base: var(--h4-base);
	  }
	  
	  @supports (font-size: 1cqi) {
	    :is(h1, .h1, h2, .h2, h3, .h3, h4, .h4, .fluid-type) {
	      font-size: min(var(--font-size-max), calc(var(--font-size-base) + var(--font-size-fluid, 3cqi)));
	    }
	  }
	  ```
- ## Using Font Size Ratio
	- ```
	  :root {
	    /*  Body font size  */
	    --body-font-size: 1rem;
	  
	    /* Compounded headlines sizes */
	    --font-size-4: calc(var(--body-font-size) * var(--type-ratio));
	    --font-size-3: calc(var(--font-size-4) * var(--type-ratio));
	    --font-size-2: calc(var(--font-size-3) * var(--type-ratio));
	    --font-size-1: calc(var(--font-size-2) * var(--type-ratio));
	  }
	  ```
- ## References
	- 1:: https://moderncss.dev/container-query-units-and-fluid-typography/