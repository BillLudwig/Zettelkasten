tags:: CSS

- ## Expensive CSS Properties
	- ### Box Shadow
		- Use smaller blur radius to reduce processing
		- Use solid color instead of gradient to greatly reduce processing
		- Use `inset` keyword for inner shadows to avoid rendering an extra layer
		- Use `will-change` for animated box shadows
	- ### Background Image
		- Use smaller image size
		- Compress!!!
		- Use image sprites to reduce HTTP requests
		- Lazy load
	- ### Border Radius
		- Surprisingly expensive for performance
		- Use smaller radius values
		- Use `border-image` if you have complex designs
	- ### Transforms
		- Use 2D transforms if possible
		- Use the `will`