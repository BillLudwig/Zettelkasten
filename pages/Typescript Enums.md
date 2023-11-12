tags:: Typescript

- All Enums are `union` enum types for good, but confusing, [reasons](https://github.com/microsoft/TypeScript/pull/50528).
  id:: 642b6cc2-1149-407c-98ba-012275489563
	- An enum declaration now declares a type representing the entire enum and types representing each member (similar to literal enum types). For example the below code declares a type `E` and types `E.A`, `E.B`, and `E.C`, where `E` is the union `E.A | E.B | E.C`.
	- ```
	  enum E {
	      A = 10 * 10,  // Numeric literal enum member
	      B = "foo",    // String literal enum member
	      C = bar(42)   // Opaque computed enum member
	  }
	  ```