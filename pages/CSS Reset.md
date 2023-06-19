tags:: CSS

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
-
- Sources:
	- 1:: https://moderncss.dev/modern-css-for-dynamic-component-based-architecture