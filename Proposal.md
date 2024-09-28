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
1. Version control: Git and GitHub will be the tools used for version tracking and uploading changes to the source code
2. Issue tracking: The Issues feature on GitHub will be the tool used for setting the goals and bringing up problems during the development process.
3. Any other technologies will be determined over the course of the project

## Product testing

### RESTful APIs testing
The way in which the RESTful APIs will be tested after their deployment in an EC2 instance will involve using a unit testing framework that will check that the two API routes defined can be used for their intended functions and that they are both returning the correct status code.

### EC2 cluster testing
The way in which the EC2 cluster will be tested after its deployment will involve using the fully functional RESTful APIs to check that the auto-scaling rules defined are responding appropriately to different stress levels of CPU and memory usage by creating or terminating different numbers of EC2 instances.

### Auto-scaling rules testing
The way in which the auto-scaling rules will be tested after their deployment for the EC2 cluster will involve analyzing their capability of scaling up and down according to different previously defined resource usage threshold and also assessing and endurance through several load tests and soak tests of varying degrees of strain.

## Estimated development timeline
1. Finishing the development of the RESTful APIs and running them through unit tests locally (weeks 1-2)
2. Creating an EC2 instance for deploying the RESTful APIs and starting to study how to define the auto-scaling rules through the AWS CLI and Terraform (weeks 1-2)
3. Deploying the RESTful APIs on the EC2 instance created and using the two API routes defined to run unit tests for each endpoint (weeks 3-4)
4. Creating an EC2 cluster for the future performance tests and starting to configure the auto-scaling rules for the previously defined resource usage thresholds (weeks 5-6)
5. Finishing configuring the auto-scaling rules for the EC2 cluster and starting to conduct load and soak tests to assess their performance (weeks 7-8)
6. Conducting more exhaustive load and soak tests for the EC2 cluster and implementing the necessary optimizations to the auto-scaling rules to create a reliable and stable E2E solution (week 9)

## Transfering deliverables to the client
After starting communications with the client, we created a GitHub organization where we have different repositories that we are going to continue using during the upcoming weeks while working on this project. The client has already been added to this organization and has full access to all of our commits. At the conclusion of the project, we will transfer the ownership of this organization to the client, which will additionally transfer ownership of all the repositories stored within to him as well.
