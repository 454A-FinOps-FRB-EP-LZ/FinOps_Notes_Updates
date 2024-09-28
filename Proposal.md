# FinOps E2E Solution

## Section 1: Overview

This project aims to create an E2E (end-to-end) solution that deploys two small applications into a cloud environment while leveraging FinOps principles to optimize cost and performance management. The goal of this project is to introduce the core principles of FinOps along with the best practices in cloud architecture, performance testing, and resource scaling that are carried out in industry. This E2E solution will include:

1. Two RESTful APIs that consume a certain percentage of CPU capability or memory amount respetively.
2. An EC2 cluster that starts with a minimum number of instances and scales up to a maximum based on auto-scaling rules.
3. Proving the auto scaling rules and evaluates resource usage through a scalability test and the stability through a soak test.

More details on each of the above will be provided in the project requirements section below.

## Client

This project is proposed by Justin Ohrenberger, Senior Manager of Cloud Platform Engineering Team at Federal Reserve Bank of St. Louis (justin.ohrenberger@stls.frb.org)

## Section 2: Project requirements
A minimal viable solution for this project includes two working RESTful APIs, a scalable EC2 cluster that demonstrates scalability and stability by passing the performance tests. 

### Minimum equirements for the RESTful APIs:
1. first RESTful API (memory): is able to detect memory amount of machine running and randomly select consuming 5/10/15/25/35 percent and simulate stress on the system by the random allocation of memory
2. second RESTful API (CPU): is able to detect CPU capability of machine running and randomly select consuming 5/10/15/25/35 percent and simulate stress on the system by the random allocation of CPU
3. deployable onto an EC2 instance to initiate testing on the cloud

Additional features worth considering if time permits:
1. establish integration between the CPU API and the Memory API
2. redesign the scability rules accordingly given any shift in performance or demand toleration

### Minimum requirements for the EC2 cluster
1. deployed onto AWS with a minimum number of instances which scale up to a maximum number of instances
2. leverages AWS CLI when working with EC2 instances and Infrastructure as Code technology (e.g. Terraform)
3. implemented with auto-scaling policies for the EC2 instances based on performance metrics formed via (CPU or memory load)

### Minimum requirements for the Auto Scaling rules
1. configured to automatically scale based on resource usage thresholds.
2. can scale both up and down
3. are able to pass load tests; these test the scalability of the rules and whether they can handle different amounts of load
4. are able to pass soak tests; these test the stability of the scaling and whether they can within stand high load for an extended duration of time

## Additional features beyond the three pieces above if time permits
Latency and fault tolerance: Establish a failover strategy for transactions that fail during peak testing that prevents lost of business due to high demand leveraging a queue driven structure (e.g. Netflix Hystrix)

## Technologies required/used for development
1. Version control - git and github.com will be used for manageing the codebase
2. Issue tracking - github issues will be used for planning and tracking rogress on project development
3. other technologies TBD based on further research