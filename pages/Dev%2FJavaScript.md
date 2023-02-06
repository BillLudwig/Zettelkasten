- ## Notes
- Compare values with `Object.is('first', 'second')` *// false*
  id:: 63ca0bfb-30ef-4d79-98af-9a0c5c6806f2
	- Similar to the `====` but understands a few differences that `===` doesn't
		- console.log(Object.is(-0, +0)); *// false*
		- console.log(Object.is(-0, -0)); *// true*
		- console.log(Object.is(NaN, NaN)); *// true*
	- Use `Number.toLocaleString` to internationalize numbers
	- Use `Intl.Segmenter` to split strings in a locale safe way
- ## Links
	- [Ultimate Guide to Javascript Error Handling](https://www.sitepoint.com/javascript-error-handling/) #Dev/JavaScript
	  id:: 63e00d7b-e2a4-4f87-afff-a241b9a0749b
		- Showing an error message is the last resort