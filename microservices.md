>>>>>>>>>Microservices vs monoliths
Users(browser, mob, webservice), FE, backend, db
Monoliths
	one change still deploye all
Microservices
	
Incremental release
Need for systematic approach
	strategy requirements
		risk elimination
		control speed
		build confidence
		release through multiple sprints
		rollback strategy
		avoid big bang - not having rollback plans,

Stragler application pattern
	tree and fig
	tree - monoliths
	fig - microservices
	tree - coexist - fig
	incremental transition
	Intercepting interactions point
		new capabilities - group of similar functions
		routing component - sits between tree and fig
		Transform - coexist - eliminate
	transform -> coexist -> release strategy -> eliminate -> rinse and repeat
	
	
>>>>>>>>> Design Principles

Course plan & Other supporting Docs - https://github.com/greenlearner01/Microservices-Architecture

--Design principles

Domain Driven Design
Hide Implementation Details
Decentralization
Failure Isolation/tolerance
discoverability
Continuous Delivery through DevOps Culture
Reuse
Autonomy

Goldilocks Principle: Not too big, not too small, and not too tightly coupled.
"A microservice should have X lines of code"
"Turn each function into a microservice"
The two-pizza principle
Is your service the right size and properly defined?
	Is there over-reliance between services?
-It doesn't share database tables with another service
-It has a minimal amount of database tables
-It's thoughtfully stateful or stateless
-Its data availability needs are accounted for
-It's a single source of truth

Define the scope properly
Design for failure
Build around business capabilities
Decentralize data
Monitor constantly
Manage traffic
Unique Source Of Identification
Minimal Database Tables

SRP
DDD
SOA
	encapsulation
	loose coupling
	separation of concern
Hexagonal architecture


--Design constraints
availability
scalability
performance
usability
flexibility

---new problems


#Characteristics of Microservices

small
stateless
Independent
Products Not Projects

>>>>>>>>> Desing Patterns
https://www.lambdatest.com/blog/design-patterns-for-micro-service-architecture/
https://dzone.com/articles/design-patterns-for-microservices
https://www.edureka.co/blog/microservices-design-patterns
https://microservices.io/microservices/news/2015/03/15/deployment-patterns.html
https://dzone.com/articles/right-strategies-for-microservices-deployment

Applying above principles gives lots of challenges to solve in microservice.
Many patterns have evolved over the time. - 

1. Decomposition patterns
	> decompostion by business capabilities
	> decompostion by subdomain
	> strangler pattern
	> bulkhead 
	> sidecar / service mesh
		https://dzone.com/articles/sidecar-design-pattern-in-your-microservices-ecosy-1
		https://dzone.com/articles/the-rise-of-service-mesh-architecture
2. Integration patterns
	> API gateway
	> Aggregator pattern
	> client side UI composition patterns
	> chained pattern
3. Database patterns
	> Database per service
	> shared database per service - suited for brownfield apps
	> CQRS
	> SAGA
	> Event Sourcing
4. Observability
	> Log aggregation
	> Performance metrics
	> Distributed tracing
	> health check
5. cross-cutting concern patterns
	> external configuration
	> service discovery pattern
	> circuit breaker pattern
	> blue green deployment
6. Communication Among services
	> Synchronous
	> Async - event/msg based
	> Communication Medium
		> HTTP REST - xml/json
		> Graphql
		>gRPC
7. Deployment patterns
https://www.dotnettricks.com/learn/microservices/deployment-patterns
https://microservices.io/microservices/news/2015/03/15/deployment-patterns.html
https://dzone.com/articles/right-strategies-for-microservices-deployment
	Multiple service instances per host - deploy multiple service instances on a host
	Service instance per host - deploy a single service instance on each host
	Service instance per VM - a specialization of the Service Instance per Host pattern where the host is a VM
	Service instance per Container - a specialization of the Service Instance per Host pattern where the host is a container
	server less 
	blue green
	canary
	PaaS
	
https://tsh.io/blog/design-patterns-in-microservices-api-gateway-bff-and-more/
>>>>>>>side car
https://docs.microsoft.com/en-us/azure/architecture/patterns/sidecar
https://samirbehara.com/2018/07/23/sidecar-design-pattern-in-your-microservices-ecosystem/
https://medium.com/@sauravomar01/sidecar-pattern-in-microservices-9599cc963dd4
>>>>>>>>>>>>Service Mesh
https://medium.com/microservices-in-practice/service-mesh-for-microservices-2953109a3c9a
https://www.redhat.com/en/topics/microservices/what-is-a-service-mesh
https://buoyant.io/2017/04/25/whats-a-service-mesh-and-why-do-i-need-one/
https://thenewstack.io/category/service-mesh/
https://www.infoq.com/articles/service-mesh-ultimate-guide/
https://www.hashicorp.com/resources/what-is-a-service-mesh/
What is a ‘Service Mesh’?
In a nutshell, a Service Mesh is an inter-service communication infrastructure.
service mesh vs api gateway
	
A typical service mesh can be divided into two parts, a data plane and a control plane. The data plane deals with the actual traffic from one application to another. Any networking aspects regarding the actual service requests, such as routing, forwarding, load balancing, even authentication and authorization are part of the service mesh data plane. The control plane is the entity that connects the various data planes into a distributed network. This is the policy and management layer of the service mesh.

>> db design patters
https://www.edureka.co/blog/microservices-design-patterns#
event sourcing  - https://docs.microsoft.com/en-us/azure/architecture/patterns/event-sourcing
	
	
	
	
