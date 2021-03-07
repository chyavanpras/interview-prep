
# [Grokking the System Design Interview](https://www.educative.io/courses/grokking-the-system-design-interview)

- [Steps to Approach Design](#steps-to-approach-design)
- [Design TinyURL](#design-tiny-url)
  - [Requirements](#tiny-url-requirement)
  - [Estimates](#tiny-url-estimates)
  - [Data models](#tiny-url-models)
  - [APIs](#tiny-url-apis)
  - [System design](#tiny-url-design)
  - [Partition](#tiny-url-partition)
  - [Cache](#tiny-url-cache)
  - [Telemetry](#tiny-url-telemetry)
  - [Security](#tiny-url-security)
- [Storage and retrieval](#storage-and-retrieval)
  - [Data structures that power up your database](#data-structures-that-power-up-your-database)
  - [Transaction processing or analytics?](#transaction-processing-or-analytics)
  - [Column-oriented storage](#column-oriented-storage)

## Steps to Approach Design

A data-intensive application is typically built from standard building blocks. They usually need to:
* Store data (_databases_)
* Speed up reads (_caches_)
* Search data (_search indexes_)
* Send a message to another process asynchronously (_stream processing_)
* Periodically crunch data (_batch processing_)

* **Reliability**. To work _correctly_ even in the face of _adversity_.
* **Scalability**. Reasonable ways of dealing with growth.
* **Maintainability**. Be able to work on it _productively_.

### Reliability

Typical expectations:
* Application performs the function the user expected
* Tolerate the user making mistakes
* Its performance is good
* The system prevents abuse

Systems that anticipate faults and can cope with them are called _fault-tolerant_ or _resilient_.


