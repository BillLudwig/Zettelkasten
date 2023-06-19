tags:: CSS

- ## Code Snippets
	- Basic Example: [^1]
		- ```
		  .container {
		    container-type: inline-size;
		  }
		  
		  .fluid-type {
		    font-size: clamp(1rem, 4cqi, 3rem);
		  }
		  ```
		- The .container wrapper is required to get the `cqi` unit to work on resize [^1]
	-
- ## References
	- 1:: https://moderncss.dev/container-query-units-and-fluid-typography/