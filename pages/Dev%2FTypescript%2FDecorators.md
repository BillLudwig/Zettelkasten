- Since: 5.0
- Reference: https://devblogs.microsoft.com/typescript/announcing-typescript-5-0/#decorators
- Example:
	- ```
	  class Person {
	      name: string;
	      constructor(name: string) {
	          this.name = name;
	      }
	  
	      @loggedMethod
	      greet() {
	          console.log(`Hello, my name is ${this.name}.`);
	      }
	  }
	  
	  const p = new Person("Ron");
	  p.greet();
	  
	  // Output:
	  //
	  //   LOG: Entering method.
	  //   Hello, my name is Ron.
	  //   LOG: Exiting method.
	  ```