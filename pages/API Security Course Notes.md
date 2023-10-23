tags:: Cyber
link:: https://university.apisec.ai/products/api-security-fundamentals
id:: 65359126-88ed-40b5-8345-0ff39bded37e

- ## API Security Fundamentals [^1]
	- ### OWASP API Security Top 10
		- [[OWASP Top Ten]]
	- ### 3 Pillars of API Security
		- #### Governance
		  collapsed:: true
			- Benefits
				- Consistancy
				- Sets expectations for engineering team
				- Establishes standard processes
				- Enforces security
			- Components
				- Awareness
					- Know Your APIs
						- Get full inventory APIs
							- Purpose, owner, documentation
						- Standardize and enforce API deployment process
							- Existence of "shadow/rogue" APIs sign of weak governance
							- APIs only deployed in approved ways, with proper validation
							- Enforce governance at Gateway, Marketplace
						- Mandate API Documentation
							- Make sure APIs are consistent and reusable
							- Define documentation requirements
						- Create API Development standards
							- Style guides, authentication requirements, versioning, PII tracking
					- Know Your Data
					- Know Your Risks — Threat Modeling
						- Identify: APIs, business flows, data, access paths
						- Assess: vulnerabilities, logic flaws, access controls, 3rd party risk
						- Probability: examine the likelihood of an attack
						- Impact: understand the damage, loss, consequences of an attack
						- Mitigation: develop a plan to address the risk
				- Policy & Process
					- Engineering Processes
					- API Documentation
						- Just Use Swagger!!
					- Design Guides: Promote Governance, Consistency
						- Authentication — type (basic, token, certificate), how to implement
						- Authorization — who has access to what, where enforced
						- Naming Conventions — URIS as nouns, Methods as verbs, pluralization, hierarchy, case, language, no jargon/abbreviations
						- Error Codes — status codes, reference ID, human readable messages
						- Versioning — when to increment, when not, types of versions
						- Units, Formats, Standards — date/time formats, timezones
		- #### Testing
		  collapsed:: true
			- "Standard playbook" test categories offer limited value
				- Cross-site scripting, injection, buffer overflow
				- Important to run these tests to avoid bot-based attacks
				- API breaches rarely exploit these
				- Major breaches typically business logic flaws
			- API Security
				- Endpints
				- Authentication exploits
				- Enumeration
				- App DOS, rate limiting
				- Missing TLS, SSL issues
				- Injection, fuzzing
				- Fuzzing, input validation
				- Server-side resource forgery
				- Server properties leaks
			- Data Security
				- Access control
				- Excessive data
				- Sensitive data
				- Personal. health, bank data
				- File, directory
				- Encryption at rest
				- Data exfiltration
			- Business Logic
				- Cross-æcount access
				- Apr function abuse
				- Role-based access control
				- Pen-testing
		- #### Monitoring
			- Runtime Protection
			  collapsed:: true
				- Policy enforcement
				- Authentication
				- Traffic filtering
			- Threat Detection
			  collapsed:: true
				- Fraudulent traffic
				- Distributed attacks
				- Incident response
			- Control Validation
			  collapsed:: true
				- Verify API controls
				- Uncover anomalies
			- Types of Monitoring
				- Proactive: Blocking
				  collapsed:: true
					- API Gateway
					- Web App Firewall
				- Reactive: Alerting
				  collapsed:: true
					- Logging, SIEM
					- Runtime API Threat Management
				- API Discovery
				  collapsed:: true
					- Monitoring can aid API inventory efforts
						- Identify API endpoints in use
						- Discover undocumented/unknown APIs
					- Comprehensive discovery requires more sources:
						- API Gateway, Web Application Firewall
						- Code repository
						- Application testing, crawling
					- Reliance on traffic based-discovery misses:
						- Internal API traffic not seen by traffic analysis tool
						- Pre-production APIs
						- Unexercised endpoints
- ## Footnotes
	- [^1]: https://university.apisec.ai/products/api-security-fundamentals