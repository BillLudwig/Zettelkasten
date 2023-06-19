tags:: Dev

- ## Notes
- Compare values with `Object.is('first', 'second')` *// false*
  id:: 63ca0bfb-30ef-4d79-98af-9a0c5c6806f2
	- Similar to the `====` but understands a few differences that `===` doesn't
		- console.log(Object.is(-0, +0)); *// false*
		- console.log(Object.is(-0, -0)); *// true*
		- console.log(Object.is(NaN, NaN)); *// true*
	- Use `Number.toLocaleString` to internationalize numbers
	- Use `Intl.Segmenter` to split strings in a locale safe way
- ## Links
	- [Ultimate Guide to Javascript Error Handling](https://www.sitepoint.com/javascript-error-handling/) #Javascript
	  id:: 63e00d7b-e2a4-4f87-afff-a241b9a0749b
		- tldr; showing an error message is the last resort
	- [Modern Errors] - small library for error handling #Javascript
	  id:: 641a5183-6764-4436-9553-8247334687ee
	- [Size-Limit](https://github.com/ai/size-limit) - Calculate the real cost to run your #Javascript app or lib to keep good performance. Show error in pull request if the cost exceeds the limit.
	  id:: 6490c517-25fb-4875-b561-3b62ae60710e
	- [knip](https://github.com/webpro/knip) - Find unused files, dependencies and exports in your #JavaScript and #TypeScript projects. Knip it before you ship it! - Going to have to start using this on my projects.
	  id:: 645da9c5-9b41-4e47-8827-fd49f3f0f714
	- [Supercluster](https://github.com/mapbox/supercluster) - A very fast #Javascript geospatial point clustering library for browsers and Node.
	  id:: 644b3ef4-dcc6-4e09-bda7-81ec59304e67
	- [FullCalendar](https://fullcalendar.io/) - #Javascript calendar with #Angular component
	  id:: 644b40a5-8600-4855-adc4-2ebf294fd7d8
	- [Signals: Fine-grained Reactivity for JavaScript Frameworks](https://www.sitepoint.com/signals-fine-grained-javascript-framework-reactivity/) - #Angular is moving to this but it's a bigger #Javascript concept.
	  id:: 64470d37-7c60-4347-8dbd-061c702a7997
	- [List.js](https://listjs.com/) - Adds search, sort, filters, etc to lists and tables #Javascript
	  id:: 6438a673-110c-44c0-939c-ff56efd3d699
	- [Chrono](https://github.com/wanasit/chrono) - natural language date parser in #Javascript
	  id:: 642b6cbe-f08d-454c-98fc-133910f66036
	- [minisearch](https://github.com/lucaong/minisearch) - Tiny and powerful full-text search engine for browser and Node #Javascript
	  id:: 642b6cbf-294d-4d09-bb5b-7d36fff21b31
	- [fast-querystring](https://github.com/anonrig/fast-querystring) - Fast query-string parser and stringifier to replace the legacy node:querystring module. #Javascript
	  id:: 642b6cbf-37c6-4124-85cf-7fad7d5085e6
	- [JSON Crack](https://jsoncrack.com/) - Tool to visualize JSON data. Has VSCode plugin #Javascript
	  id:: 642b6cbf-1cb8-4494-8285-092250083217
	- [memlab](https://facebook.github.io/memlab/): Memory testing framework for finding memory leaks for [[Javascript]]
	  id:: 642b6cbf-8cad-4b59-8173-2050050c94de
	- [Blueboat](https://blueboat.io/) is a serverless multi-tenant [[Javascript]] runtime.
	  id:: 642b6cbf-d72e-4d35-8ee9-66db0ae80b9e
	- [tesseract](https://github.com/naptha/tesseract.js) [[Javascript]] library for extracting text from images.
	  id:: 642b6cbf-c3f9-43d2-b7e1-664850a8657d
	- [Hyper Fetch](https://hyperfetch.bettertyped.com/) looks interesting as a state management solution for [[Javascript]] or [[Typescript]].
	  id:: 642b6cbf-efad-442d-8185-031755ad92dd
	- [DgrmJS](https://github.com/AlexeyBoiko/DgrmJS) [[Javascript]] library for creating SVG flow diagrams
	  id:: 642b6cc0-fb09-4d71-8b65-2e7311efb1a2