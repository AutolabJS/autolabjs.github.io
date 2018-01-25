---
layout: page
title: DevOps Integration
permalink: /gsoc/devops/
tags: gsoc devops
---
**Project Title**: Integrate DevOps Practices into AutolabJS

**Description**: AutolabJS project has been created in the spirit of Microservices architecture. That is why the work done is distributed across five service components, namely Main Server, Load Balancer, Execution Node, MySQL DB and GitLab. Of the five components, MySQL DB and GitLab are used as fully packaged components. The other three components (Main Server, Load Balancer and Execution Node) are created and maintained as part of AutolabJS project.

We want to introduce the following DevOps principles into the AutolabJS.
1. Principle of Flow - Continuous delivery of software from developers to installations. In order to realize the principle of flow in AutolabJS, we need to implement the following features
    * Functional, Integration and Unit tests: The tests would give confidence about all the code and functionality put in the project. Once the tests are in place, we can hope to achieve the next principle.
    * Continuous deployment: One step installation and one step update of AutolabJS software. In order to realize these two goals, we need to release AutolabJS software automatically for each build (continuous delivery). There must also be a mechanism for hot update all the components of AutolabJS (continuous deployment)  
1. Principle of Feedback - Continuous collection of data from deployments to provide insights to all participants
    * Telemetry: Setup a proper log and metrics dashboard system for AutolabJS installation so that the administrator, instructor and students of an AutolabJS installation have clear picture of the state of the system. The logs and metrics are also aggregated, anonymized and transferred to AutolabJS development team.
    * Feature Toggles: AutolabJS needs configuration driven low-risk feature deployment.

**Difficulty Level**: Medium

**Mentor(s)**: [Ankshit Jain](https://github.com/AnkshitJain) (f20150006 AT goa DOT bits-pilani DOT ac DOT in), [Prasad Talasila](https://github.com/prasadtalasila) (tsrkp AT goa DOT bits-pilani DOT ac DOT in)

**Main Goals**:
* Functional, integration and unit tests for all the components
* One-step installation
* One-step update
* Logs
* Metrics with Dashboard

**Deliverables**:
* 100% code coverage separately for functional, integration and unit tests
* Atomic installation of AutolabJS (i.e., multiple installations do not effect the existing application data)
* A deb package for AutolabJS
* System in place to autogenerate the deb package for each successful build of AutolabJS
* Migration of all console-based logs to Logger.js based system for all the AutolabJS components
* A dashboard for AutolabJS installation which shows the status of all the components and the submitted jobs
* One commandline option to update AutolabJS.
* One commandline option to export AutolabJS logs to a zip file.

**Relevant Issues**: [GSoC-DevOps](https://github.com/AutolabJS/AutolabJS/labels/GSoC-DevOps)

**Skills Required**: ES6 Programming on Node.js 8.x, [JS Testing](https://github.com/AutolabJS/AutolabJS/wiki/Testing), Ansible, Deb packaging, Winston logger

**Getting Started**:
1. Install AutolabJS and run a sample lab.
1. Improve some aspect of installation by taking care of problems listed in issues with [install](https://github.com/AutolabJS/AutolabJS/labels/install) label.
1. Write tests to satisfy at least some of the problems raised in issues with [tests - missing](https://github.com/AutolabJS/AutolabJS/labels/tests%20-%20missing) label.


**Administrator**: [Prasad Talasila](https://github.com/prasadtalasila) (tsrkp AT goa DOT bits-pilani DOT ac DOT in)

**References**:

1. The DevOps Handbook, Gene Kim et al., IT Revolution Press, 2016.
1. [CI vs CD](https://www.atlassian.com/continuous-delivery/ci-vs-ci-vs-cd)
