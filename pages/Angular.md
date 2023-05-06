tags:: WebDev

- ## Router
	- Router data as component @Input() added in v16 (this is really cool)
		- https://angular.io/api/router/withComponentInputBinding
	- Functional Router Guards should reduce boilerplate Since 15
		- Can run guards in sequence. [See test code](https://github.com/angular/angular/blob/8546b17adec01de69bf314a959ef2d12f6638eb9/packages/router/test/integration.spec.ts#L5157-L5194)
	- [Advancements in the Angular Router](https://blog.angular.io/advancements-in-the-angular-router-5d69ec4c032) Since 14.2
		- Better tree-shaking in the Router removing the old `HashLocationStrategy` and SSR code if not used
			- Saves about 11% of the router code size
		- No longer need to import RouterModule directly.
			- New: `providers: [provideRouter(appRoutes)]`
			- Old: `providers: [importProvidersFrom(RouterModule.forRoot(appRoutes))]`
		- No longer need to have the `.then(m => m.Component)` boilerplate as these are unwrapped by default.
- ## Signals (since v16)
  id:: 6446f9d8-e843-4046-808f-e610f213bbef
	- Core Concepts aka Reactive Primitives
		- signal - like a variable but notifies Angular when it changes
		- computed - calculates value based on signals and notifies Angular when the calculated value changes
		- effect - functions that executes whenever the signal they use changes
	- `zone.js` is still needed for now (as of v16)
	- Might need `@angular/core/rxjs-interop` with v16 but unclear
		- TODO: Investigate RXJS/Angular Signals
	- Links to check out
		- ((64470d37-7c60-4347-8dbd-061c702a7997))
		- [Sub-RFC 3: Signal-based Components](https://github.com/angular/angular/discussions/49682)
	- Videos to watch
		- [Angular is about to get its most IMPORTANT change in a long time...](https://www.youtube.com/watch?v=4FkFmn0LmLI) - Good overview of Signals by Joshua Morony
		- [Why didn't the Angular team just use RxJS instead of Signals?](https://www.youtube.com/watch?v=iA6iyoantuo) - More about Signals vs RxJS from Joshua Morony
- ## Standalone APIs (Since v15)
	- A way to create components that do not need to be included into a ngModule.
		- https://angular.io/guide/standalone-components
		- ```
		  @Component({
		  	standalone: true,
		      selector: 'app-component',
		      imports: [Imports go here instead of in a module]
		  })
		  ```
	- Standalone migration schematics added in v16
		- `ng generate @angular/core:standalone`
		- `ng new my-app --standalone`
- ## Misc Notes
	- [Image Directive](https://developer.chrome.com/blog/angular-image-directive/) is now stable since v15 and does automatic `srcset` generation
- ## References
	- ### Forms
		- [Safer Forms With Strict Types](https://www.youtube.com/watch?v=Z-vwuG_szVk) [[Angular]] [[Video]] by Dylan Hunn via ng-conf. #[[November 17th, 2022]]
		  id:: 6377ab08-b007-4bf0-bb3d-d5e116a444bd
-