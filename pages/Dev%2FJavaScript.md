- ## Notes
- Compare values with `Object.is('first', 'second')` *// false*
  id:: 63ca0bfb-30ef-4d79-98af-9a0c5c6806f2
	- Similar to the `====` but understands a few differences that `===` doesn't
		- console.log(Object.is(-0, +0)); *// false*
		- console.log(Object.is(-0, -0)); *// true*
		- console.log(Object.is(NaN, NaN)); *// true*