# API Testing

#### What
- Tests the API layer.

#### API Layer
- It is the channel which connects client to server (or one microservice to another), drives business processes, and provides the services which give value to users. 

#### Why
- A customer-facing public API that is exposed to end-users becomes a product in itself. If it breaks, it puts at risk, not just a single application, but an entire chain of business processes built around it. 

#### Benefits
- Fast
- High ROI
- Simplify business logic validation
- Complete user story coverage
- Essentially end to end tests without the brittleness of UI tests.

#### What to test / Test Strategy
- Functional Testing
	- ensure it works correctly as expected
	- ensure it works as specified to requirement specification (becomes API Docs)
	- prevent regressions between code merges and releases
- Contract Testing (Swagger or OpenAPI)
	- ensures endpoints are correctly named
	- ensures resources and their types correctly reflect the object model
	- ensures there is no missing or duplicate functionality
	- relationships between resources are reflected in the API correctly
	- check [Semantics], [Conventions], and [Principles]

#### Test Scenario
- Basic positive tests
- Extended positive testing with optional parameters
- Negative testing with valid input
- Negative testing with invalid input
- Destructive testing (optional)
- Security, authorization, and permission tests (optional)

#### Test Case Steps
- Verify correct HTTP status code
- Verify response payload
- Verify response headers
- Verify correct application state (optional)
- Verify basic performance sanity



[Semantics]: <https://techbeacon.com/app-dev-testing/guide-restful-api-design-35-must-reads>
[Conventions]: <https://restfulapi.net/rest-api-design-tutorial-with-example/>
[Principles]: <https://hackernoon.com/restful-api-designing-guidelines-the-best-practices-60e1d954e7c9/>