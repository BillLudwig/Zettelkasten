- ## Misc Notes
	- Since 5.0 All Enums are `union` enum types for good, but confusing, [reasons](https://github.com/microsoft/TypeScript/pull/50528).
		- An enum declaration now declares a type representing the entire enum and types representing each member (similar to literal enum types). For example the below code declares a type `E` and types `E.A`, `E.B`, and `E.C`, where `E` is the union `E.A | E.B | E.C`.
		- ```
		  enum E {
		      A = 10 * 10,  // Numeric literal enum member
		      B = "foo",    // String literal enum member
		      C = bar(42)   // Opaque computed enum member
		  }
		  ```
	-
- ## Assignment Operators
	- [[Dev/Typescript]] v4.0 supports three new assignment operators  for logical and `&&=`, logical or `||=`, and nullish coaliscing `??=`. This is perfect for writing more ~~confusing~~ concise code.
	  id:: 63936b73-9316-4975-8049-a60fd1e78b7d