---
layout: page
title: Architectural Improvements
permalink: /gsoc/arch/
tags: gsoc architecture
---
**Project Title**: Architectural Improvements to AutolabJS

**Description**:
The existing architecture of AutolabJS needs further improvements to take it to next level of supporting 50 to 5000 concurrent users. One of the major problems in the current architecture is the transaction guarantees. For us each evaluation is a transaction. We need to implement atomic transactions.

The interfaces of all the AutolabJS components need to be improved to comply with the REST API requirements. When implementing the new API, we must make provision for version control and gradual deployment of REST API.

The new system should propose a way of distributing the execution nodes across the Internet. The load balancer should take up the job of distributing the evaluation job requests and receiving the responses from execution nodes. Obviously, with Internet being what it is, we need to account for message delays, job failures, malicious participants.

Any proposed architecture must fully comply with DevOps practices and must adhere to the principles of microservices.

**Difficulty Level**: Hard

**Mentor(s)**: [Ankshit Jain](https://github.com/AnkshitJain) (f2015006 AT goa DOT bits-pilani DOT ac DOT in), [Prasad Talasila](https://github.com/prasadtalasila) (tsrkp AT goa DOT bits-pilani DOT ac DOT in)

**Mail Goals**:
* Design and implementation of clean REST interfaces
* Transaction guarantees in the system
* Scalable message distribution among load balancer and execution node clusters
* Resilience against failures
* Implementation of Exam mode
* Protection against network intrusions

**Deliverables**:
A new architecture in code that provides testable guarantees of the following features.
* clean REST API with versioning in place
* Ability to scale the number of execution nodes from 1 to 1000
* Atomic evaluations
* Protection against network attacks on different components of the architecture
* Ability of the system to sustain downtime for all the components and gracefully degrade performance
* Secure examination mode which hides all the existing code base for the duration of the test



**Relevant Issues**: [GSoC-Arch](https://github.com/AutolabJS/AutolabJS/labels/GSoC-Arch)

**Skills Required**:
1. Implementations of microservices Architectures using Node.js stack (may be feathers.js, seneca.js etc.)
1. DevOps Pratices (eventual consistency using redis, winston for logs, statsd and graphite components)
1. Messaging systems (preferably zeromq or pattern matching as used in seneca.js / feathers.js etc.)


**Getting Started**:
1. Install AutolabJS and run a sample lab.
1. Improve some aspect of the existing execution node by taking care of problems listed in issues with [GSoC-Arch](https://github.com/AutolabJS/AutolabJS/labels/GSoC-Arch) label. This demonstrates your understanding of the existing code base.
1. Create a skeleton code structure for implementing your proposal and write functional, integration and unit tests for your code structure.


**Administrator**: [Prasad Talasila](https://github.com/prasadtalasila) (tsrkp AT goa DOT bits-pilani DOT ac DOT in)
