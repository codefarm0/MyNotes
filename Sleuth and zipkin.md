## Agenda
	### Distributed tracing
		Critical tool for debugging and understanding microservices
	###Request Tracing
	### Latency Issues
	### What is Sleuth and its potential
	### Visualizing logs in distributed systems
	
	
	
## Intro
	Suppose customer is going to order a card on netspend.com
	He encounters error
	Reaches to customercare
	customercare reaches to prod support
	prod support reaches to QA
	QA approaches to developer
	developer reaches to logs and logs(debug)
	
## Microservice in internet giant systems
		Netflix--
		https://image.slidesharecdn.com/microservices-santoli-milano-2015-160331092750/95/microservices-architectures-become-a-unicorn-like-netflix-twitter-and-hailo-63-638.jpg?cb=1459581256
		https://contiv.io/articles/microservice-challenge-b139e7b3.jpg
		
## latency issues
	###What was the event?
	### How long did it take?
	### Why it take so long
	### How do I know it's slow
	### Which microservice is responsible
	
## Distributed tracing
	### DT is process of collecting end-to-end trancsation graphs
	###Trace - entire journey of request
	### Span - unit of work. Represents single operation call
	### DT systems are often used for this purpose. e.g. Zipkin
	###Tracers - add login to create unique trace and span id
	###Dapper paper by Google - It's prod distributed systems tracing infrastructure
	
## Visualizing Trace and spans
	### Service1 trac id 1, span id 1 
	### Service2 trac id 1, span id 2 parent span id 1 
	### Service3 trac id 1, span id 3 parent span id 2
	### Service4 trac id 1, span id 4  parent span id 2

## Tracers : Spring cloud sleuth
	### Adds traces and span ids to SLF4J MDC
	### Traces have instrumentation and sampling policy
	### Loosely based on HTrace, but zipkin(Dapper) compatible
	
## Demo for Sleuth - tracer
	SShing and grep to log files
	
	
	--
	-
	-
	-
	-
	-
	-
## Zipkin
	###distributed tracing systems
	### Implementation based on Dapper paper by Google
	### Aggregates spans into trace tree	
	### Colelction as well as lookup of data
	### 2015, OpenZipkin became the primary fork
	
## Zipkin architecture
	
	https://1.bp.blogspot.com/-AKsNvRFeGZs/V0Gdyo2ba3I/AAAAAAAABXQ/xGe8dMxakjocw5wcd4RHMHrfOqD5Q3h-ACLcB/s1600/0ca67162-0a69-11e6-9971-f47854ffb9c1.png
	
	https://image.slidesharecdn.com/distributedtracingvelocity2016-160922181728/95/distributed-tracing-velocity2016-13-638.jpg?cb=1474568294
	
## show build.gradle of applications for demo
	spring.sleuth.sampling.percentage=1.0
	logging.level.org.springframework.cloud.sleuth=debug

## Important links 
* https://www.youtube.com/watch?v=jkSm-652UPo&t=1661s
* https://www.slideshare.net/SpringCentral/how-to-properly-blame-things-for-causing-latency
* https://youtu.be/5jNVtWvN8CM?t=324
	
	
		
		