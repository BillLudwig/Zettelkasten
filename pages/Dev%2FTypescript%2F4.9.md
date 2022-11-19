title:: Dev/Typescript/4.9

- ## Changes
	- **New** Satisfies Operator
		- [Typescript's new 'satisfies' operator](https://medium.com/@cefn/typescript-satisfies-6ba52e74cb2f) by Cefn Hoile
		- [Github issue with feature request](https://github.com/microsoft/TypeScript/issues/47920)
		- TODO Read about this because it feels unnecessary and reminds me of duck typing with better errors.
	- [Unlisted Property Narrowing with the `in` Operator](https://devblogs.microsoft.com/typescript/announcing-typescript-4-9/#unlisted-property-narrowing-with-the-in-operator)
	- [Auto-Accessors in Classes](https://devblogs.microsoft.com/typescript/announcing-typescript-4-9/#auto-accessors-in-classes) adds support for an upcoming ECMAScript feature.  See [proposal](https://github.com/tc39/proposal-grouped-and-auto-accessors)
		- `accessor name: string` is just like a `get` and `set` with a private backing property.
	- **New** Will throw error when doing equality checks against `NaN` instead of using `Number.isNan`