## Part I. Foundations of Data Systems

### Chapter 1. Reliable, Scalable and Maintainable Applications

A data-intensive application is typically built from standard building blocks that provide commonly needed functionality
- Databases
- Caches
- Search Indexes
- Stream processing: send a message to another process, to be handled asynchronously
- Batch processing

Now, a single tool can no longer meet all requirements, the work is broken down into tasks that can be performed efficiently on a single tool, **those different tools are stiched together using application code**

Ex: with an application has caching layer (Memcached) and full-text search engine (Elasticsearch), application code's responsibility to keep those caches and indexes in sync with the main database

Service interface or API usually hides those implementation details from clients.

Tricky questions when desiging a data system/ service
- About data remains correct and complete even when things go wrong internally
- Provide consistently good performance to clients, even when parts of your system are degraded
- Handle an increase in load
- A good API for the service look like

We focus on three concerns that are important in most software systems:
**1. Reliability**
- App performs the function that the user expected
- Tolerate the user making mistaks or using the software in unexpected ways
- Performance is good enough for the required use case
- Prevent any unautoized access and abuse

It only make sense to talk about tolerating *certain types* of faults

Fault vs Failure
- **Fault** is defined as one component of the system deviating from its spec
-- **Hardware Faults**: quickly come to mind when we think of causes of system failure. Our first response is usually to add redundancy to individual hardware components in order to reduce the failure rate of the system.
-- **Software Errors**
- **Failure** is when the system as a whole stops providing the required service to the user

**2. Scalability**



**3. Maintainability**

