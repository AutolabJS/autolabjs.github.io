---
layout: page
title: Execution Node Cluster
permalink: /gsoc/en/
tags: gsoc execution node
---
**Project Title**: Secure, concurrent evaluation of code in execution node.

**Description**: The [execution node](https://github.com/AutolabJS/AutolabJS/tree/master/execution_nodes) component is responsible for evaluation of user code submissions. The execution node receives evaluation request from the load balancer component, forks a separate process to execute the all the user testcases in sequential order. We can speed up the execution by performing concurrent execution of the tests.

Another area of improvement is the specification of configuration for evaluation. The configuration is ad-hoc, text-file based one. We need to move to an industry standard yaml-based configuration format.

Another area of improvement is in terms of secure execution. We need hard, provable guarantees on the execution environment. Even if malicious code comes in for evaluation, we need to make sure that the code does not corrupt the execution node.



**Difficulty Level**: Medium

**Mentor(s)**: [Rajat Agarwal](https://rajat503.github.io/) (f20130866 AT goa DOT bits-pilani DOT ac DOT in), [Prasad Talasila](https://github.com/prasadtalasila) (tsrkp AT goa DOT bits-pilani DOT ac DOT in)

**Main Goals**:
* Concurrent execution of tests
* YAML configuration for execution nodes
* Secure execution in containers in even hostile environment
* Caching of instructor solution for evaluation
* Secure upload of evaluation results

**Deliverables**:
A completely new execution node component with the following features:
* Dynamic loading of configuration information
* Support for YAML configuration of execution nodes
* Secure execution of code in containers in even hostile environment
* Concurrent execution of all the tests in an evaluation
* Caching of instructor solution for evaluation
* Secure upload of evaluation results

**Relevant Issues**: [GSoC-EN](https://github.com/AutolabJS/AutolabJS/labels/GSoC-EN)

**Skills Required**: ES6 Programming on Node.js 8.x, [JS Testing](https://github.com/AutolabJS/AutolabJS/wiki/Testing), Cluster programming in Node.js, Winston logger, Microservices in Node.js, Docker containers

**Getting Started**:
1. Install AutolabJS and run a sample lab.
1. Improve some aspect of the existing execution node by taking care of problems listed in issues with [GSoC-EN](https://github.com/AutolabJS/AutolabJS/labels/GSoC-EN) label. This demonstrates your understanding of the existing code base.
1. Write functional / unit / integration tests for [execution node](https://github.com/AutolabJS/AutolabJS/tree/master/execution_nodes) component.
1. Create a skeleton code structure for concurrent, secure evaluation of code submissions.


**Administrator**: [Prasad Talasila](http://prasad.talasila.in) (tsrkp AT goa DOT bits-pilani DOT ac DOT in)
