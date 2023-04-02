- ## Update Notes
	- ### 5.0 Changes
		- All Enums are `union` enum types for good, but confusing, [reasons](https://github.com/microsoft/TypeScript/pull/50528).
			- An enum declaration now declares a type representing the entire enum and types representing each member (similar to literal enum types). For example the below code declares a type `E` and types `E.A`, `E.B`, and `E.C`, where `E` is the union `E.A | E.B | E.C`.
			- ```
			  enum E {
			      A = 10 * 10,  // Numeric literal enum member
			      B = "foo",    // String literal enum member
			      C = bar(42)   // Opaque computed enum member
			  }
			  ```
		- Typescript supports [[Typescript Decorators]] which are pretty cool for wrapping up common functionality.
	- ### 4.9 Changes
	  id:: 63a3a25a-ef21-4da8-a7d1-475b974fea2a
		- **New** Satisfies Operator
			- [Typescript's new 'satisfies' operator](https://medium.com/@cefn/typescript-satisfies-6ba52e74cb2f) by Cefn Hoile
			- [Github issue with feature request](https://github.com/microsoft/TypeScript/issues/47920)
			- TODO Read about this because it feels unnecessary and reminds me of duck typing with better errors.
		- [Unlisted Property Narrowing with the `in` Operator](https://devblogs.microsoft.com/typescript/announcing-typescript-4-9/#unlisted-property-narrowing-with-the-in-operator)
		- [Auto-Accessors in Classes](https://devblogs.microsoft.com/typescript/announcing-typescript-4-9/#auto-accessors-in-classes) adds support for an upcoming ECMAScript feature.  See [proposal](https://github.com/tc39/proposal-grouped-and-auto-accessors)
			- `accessor name: string` is just like a `get` and `set` with a private backing property.
		- **New** Will throw error when doing equality checks against `NaN` instead of using `Number.isNan`
		- [File watching improvements](https://github.com/tc39/proposal-grouped-and-auto-accessors)
		- Finally added remove unused/sort imports command for IDEs
	-
- ## Assignment Operators
	- [[Typescript]] v4.0 supports three new assignment operators  for logical and `&&=`, logical or `||=`, and nullish coaliscing `??=`. This is perfect for writing more ~~confusing~~ concise code.
	  id:: 63936b73-9316-4975-8049-a60fd1e78b7d
-