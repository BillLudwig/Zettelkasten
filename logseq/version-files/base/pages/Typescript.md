tags:: Dev

- [[Satisfies Operator]]
- ## Update Notes
	- ### 5.1 (Still in Beta)
		- [Unrelated Types for Getters and Setters](https://devblogs.microsoft.com/typescript/announcing-typescript-5-1-beta/#unrelated-types-for-getters-and-setters) - Very nice because the current implementation is a bit of a pain.
	- ### 5.0 Changes
		- Typescript supports [[Typescript Decorators]] which are pretty cool for wrapping up common functionality.
		- ((642b6cc2-1149-407c-98ba-012275489563))
	- ### 4.9 Changes
	  id:: 63a3a25a-ef21-4da8-a7d1-475b974fea2a
		- [Unlisted Property Narrowing with the `in` Operator](https://devblogs.microsoft.com/typescript/announcing-typescript-4-9/#unlisted-property-narrowing-with-the-in-operator)
		- [Auto-Accessors in Classes](https://devblogs.microsoft.com/typescript/announcing-typescript-4-9/#auto-accessors-in-classes) adds support for an upcoming ECMAScript feature.  See [proposal](https://github.com/tc39/proposal-grouped-and-auto-accessors)
			- `accessor name: string` is just like a `get` and `set` with a private backing property.
		- **New** Will throw error when doing equality checks against `NaN` instead of using `Number.isNan`
		- [File watching improvements](https://github.com/tc39/proposal-grouped-and-auto-accessors)
		- Finally added remove unused/sort imports command for IDEs
		- ((642b6cc2-77e8-420f-9123-06bf0fd7233a))
	-
-