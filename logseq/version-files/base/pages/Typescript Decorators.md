tags:: Typescript

-
- ((64470ff6-8fd7-4686-91d5-31279a479e22))
- Reference: https://devblogs.microsoft.com/typescript/announcing-typescript-5-0/#decorators
- Details
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