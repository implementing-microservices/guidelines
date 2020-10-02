If you are creating many microservices, in a microservice architecture, having some consistency in how each service is built can go a long way. 
We recommend using Makefiles for this purpose and stardandizing on common Make targets. 
This way developers that move from a service to another service will easily know how to work with your microservices, regardless of which language 
and tech stack they are implemented in.

We recommend defining and implementing following standard targets:

- start - run the code
- stop - stop the code
- build - build the code (typically: container image)
- clean - clean all caches and run from scratch
- add-module
- remove-module
- dependencies - ensure all modules declared in dependency management is
installed.
- test - run all tests and produce coverage report
- tests-unit - run only unit tests
- tests-at - run only acceptance tests
- lint - run a linter to ensure conformance of coding style with defined standards
- migrate - run database migrations
- add-migration - create a new database migration
- logs - show logs (from within the container)

## Examples:

- Go: https://github.com/inadarei/justgo-microservice
- Node: https://github.com/inadarei/nodebootstrap-microservice
