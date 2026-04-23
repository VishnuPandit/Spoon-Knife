FR = Functional Requirement

NFR = Non Functional Requirement

Requirement (FR/NFR)	API Gateway Needed	API Gateway Not Required
Single Entry Point	
Unified endpoints for multiple services, simple client integration

Few Services -> direct client-to-service communication

Routing & Service Discovery	
Routes requests to correct service instance, supports blue/green or canary deployments

If static endpoints or few services, discovery not needed

API Composition	
Gateway can combine functions from multiple services into one composite API

Client or backend service handles aggregation

Protocol Translation	
Translate  (REST <-> SOAP <-> gRPC <-> GraphQL) 

Uniform protocol stack, no translation needed

Version Management	
Gateway exposes stable API versions while backend evolves

If backend APIs rarely change

Traffic Shaping / QoS	
Routing by user type, device

Simple round-robin routing or something which a Load Balancer can do 

Security	
Centralized authN/authZ, rate limiting, WAF. API key validation

Security is built into the app(s), trusted internal environment

Performance and Stability	
Built-in caching, throttling, load balancing, aSync support

Caching / scale not required or done elsewhere

Observability	
Centralized Logging, Monitoring, KPI (Metrics), Traceability required at the entry point

Non-centralized / distributed Logging & Monitoring is acceptable

Reliability	
Circuit breakers, retries, failover policies applied consistently

Each service handles resilience

Compliance & Governance 	
Enforcing organization-wide policies, auditing, SLAs

No regulatory/compliance drivers

