# Oracle role research — Principal Software Development Engineer, requisition 348887

Research date: November 3, 2026

## Posting at a glance
Oracle’s posting is titled **Principal Software Development Engineer**, requisition **348887**, in Nashville, Tennessee. It is a regular, on-site, individual-contributor opening with relocation available. The listing calls for 6–10+ years of experience and centers the work on the foundation of Oracle Cloud Infrastructure Object Storage.

The job description calls for designing, building, and operating highly available, durable, globally distributed object storage. Its technical focus includes metadata, data placement, replication, lifecycle management, and durability workflows. It also asks the engineer to improve availability, consistency, performance, and operational simplicity; build fault isolation, automated remediation, disaster recovery and capacity-planning capabilities; collaborate across teams; lead incident root cause work; improve observability and tooling; and contribute to security, design reviews, and mentoring.

## Reading the engineering scope
This is a principal-level individual-contributor role with broad technical influence. The work spans the request path and the operating model: API behavior and compatibility, metadata decisions, placement across failure domains, replication and repair, performance under concurrency, and the signals and automation used to keep the service healthy.

The emphasis on durability workflows and fault isolation suggests that failure handling is a first-class design concern. Practical work can include testing partial failures, reasoning about consistency and idempotency, preserving safe retries, tuning Java/JVM behavior, and reducing the time needed to detect, isolate, and remediate incidents. That interpretation is an inference from the listed responsibilities and Oracle’s public reliability guidance; it does not claim knowledge of a private team charter.

## Oracle and OCI context
Oracle Cloud Infrastructure presents its cloud platform as a set of compute, storage, networking, database, and container services. Oracle describes OCI Object Storage as strongly consistent and scalable, and states that its durability design uses redundancy, failure isolation, fast recovery, and service-managed replication or erasure coding across storage servers and failure-isolation groups. Oracle’s public architecture guidance also organizes design around security and compliance, reliability and resilience, performance and cost optimization, operational efficiency, and distributed cloud. Its reliability guidance recommends avoiding single points of failure and describes disaster recovery across regions using asynchronous replication for infrastructure and data services.

For this role, those themes connect directly to data placement, replication policy, failure-domain boundaries, recovery behavior, and operational controls. A successful storage design has to preserve clear contracts for clients while making changes, failures, and repair observable to the people operating it. Oracle’s published durability characteristics describe its platform, not the candidate’s personal results.

## Resume-to-role evidence
The supplied resume gives concrete evidence that maps to the posting:

- **Availability and latency:** a multi-region Java metadata and placement service with Raft leader election and quorum replication; 99.99% availability and sub-150 ms p99 at 5× peak traffic.
- **Durability and recovery:** replication, erasure-coding repair, lifecycle workflows, and zero data loss across three simulated zone failures.
- **Performance engineering:** 2.8× throughput and 45% lower p99 latency after profiling concurrent Java, tuning JVM garbage collection and memory, and removing lock contention.
- **Operations:** metrics, logs, tracing, alerts, and automated remediation associated with 45% lower MTTR and 35% fewer paged incidents.
- **Cloud reliability:** cross-region disaster recovery, asynchronous replication, automatic failover and fault-isolation cells; RPO under one minute in drills.
- **API and event design:** backward-compatible REST/gRPC APIs with idempotency keys, retry backoff, and Kafka event processing.
- **Testing and technical leadership:** 25+ consistency and durability defects caught before production through fault-injection tests; cross-team metadata sharding, design reviews, capacity planning, and mentoring.

The strongest portfolio anchors are **Strata**, a C++ distributed object-storage server, and **Keystone**, a Go transactional metadata store. Together they make the storage, metadata, consistency, and control-plane interests legible alongside the work history.

## Public sources
- [Oracle Careers — requisition 348887](https://careers.oracle.com/en/sites/jobsearch/job/348887/)
- [OCI Object Storage FAQ](https://www.oracle.com/cloud/storage/object-storage/faq/)
- [Oracle Cloud Infrastructure](https://www.oracle.com/cloud/)
- [OCI Cloud Architecture Center](https://www.oracle.com/cloud/architecture-center/)
- [Oracle Cloud Adoption Framework — Extreme Reliability](https://docs.oracle.com/en-us/iaas/Content/cloud-adoption-framework/extreme-reliability.htm)
- [Oracle Careers — Engineering and Development](https://www.oracle.com/careers/opportunities/engineering-development/)

