---
layout: page
title: Modular Load Balancer
permalink: /gsoc/lb/
tags: gsoc load balancer
---
**Project Title**: Create new load balancer with support for plug-ins

**Description**: The load balancer is a very crucial component in AutolabJS. At the moment, the load balancer suffers from lack of proper job management. We wish to check the incoming evaluation requests for duplication, and subject all the pending evaluation requests to a timeout function. This kind of job management functionality is best offered as a plugin to the load balancer. Hence the need for plugins. Of course, the plugin structure to be proposed must be compatible with the microservices architecture that's already in the system.

At present, there is a main server module which is responsible for serving static files and terminating socket.io requests. We need to separate the static files from main server and fold the socket.io termination code into the load balancer. One proposal would be to make the socket.io handling part and the job management part into main server. We can move all the static website serving to static webserver like Apache / NGNIX.

We also have a need to backup all the student submissions at the end of the lab so that we have a snapshot of the code submitted to the lab. Another frequent feature request is to have a facility for bulk evaluation of labs. The bulk evaluation requires instructor credentials; Once started, the bulk evaluation completes the evaluation of all the registered students who submitted the lab.

**Difficulty Level**: Medium

**Mentor(s)**: [Rajat Agarwal](https://rajat503.github.io/) (f20130866 AT goa DOT bits-pilani DOT ac DOT in), [Prasad Talasila](https://github.com/prasadtalasila) (tsrkp AT goa DOT bits-pilani DOT ac DOT in)

**Main Goals**:
* Pluggable queue / job management
* Polyglot DB support
* Time machine module
* Fold the request handling part of main server into load balancer
* Support for bulk revaluation

**Deliverables**: A brand new replacement for the existing load balancer with the following features:
* Has all the functions of the existing load balancer
* Dynamic loading of configuration information
* Has a plugin system which is compatible with the microservice architecture.
* Supports a queue / job management system which is robust to failures, repetitive submissions and excess load conditions.
* Supports secure management of execution nodes; tolerates the failures of execution nodes and executes evaluation requests successfully.
* Logs all the evaluation requests and results to database
* Supports bulk evaluation requests.
* Supports a time machine module where by the user repositories of interest are copied and backed up.
* Supports registered students by checking all the incoming evaluations against a DB table of all the registered students.

**Relevant Issues**: [GSoC-LB](https://github.com/AutolabJS/AutolabJS/labels/GSoC-LB)

**Skills Required**: ES6 Programming on Node.js 8.x, [JS Testing](https://github.com/AutolabJS/autolabcli/wiki/Testing-in-JavaScript), Winston logger, Microservices in Node.js

**Getting Started**:
1. Install AutolabJS and run a sample lab.
1. Improve some aspect of the existing load balancer by taking care of problems listed in issues with [GSoC-LB](https://github.com/AutolabJS/AutolabJS/labels/GSoC-LB) label. This demonstrates your understanding of the existing code base.
1. Write functional / unit / integration tests for [load balancer](https://github.com/AutolabJS/AutolabJS/tree/master/load_balancer) component.
1. Create a skeleton code structure for plugin system that is compatible with microservices architecture.


**Administrator**: [Prasad Talasila](http://prasad.talasila.in) (tsrkp AT goa DOT bits-pilani DOT ac DOT in)
