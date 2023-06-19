tags:: Dev

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
	- [Ultimate Guide to Javascript Error Handling](https://www.sitepoint.com/javascript-error-handling/) #Javascript
	  id:: 63e00d7b-e2a4-4f87-afff-a241b9a0749b
		- tldr; showing an error message is the last resort
	- [Modern Errors] - small library for error handling #Javascript
	  id:: 641a5183-6764-4436-9553-8247334687ee
	- [Size-Limit](https://github.com/ai/size-limit) - Calculate the real cost to run your #Javascript app or lib to keep good performance. Show error in pull request if the cost exceeds the limit.
	- ((645da9c5-9b41-4e47-8827-fd49f3f0f714))
	- ((644b3ef4-dcc6-4e09-bda7-81ec59304e67))
	-