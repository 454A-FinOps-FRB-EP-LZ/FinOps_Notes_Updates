# FinOps E2E Solution

## Section 1: Overview

This project aims to create an E2E (end-to-end) solution that deploys two small applications into a cloud environment. The goal of this project is to introduce the core principles of FinOps along with the best practices in architecture and performance testing that are carried out in industry. This E2E solution will include:

1. An EC2 cluster that starts with a minimum number of instances and scales up to a maximum based on auto-scaling rules.
2. Two RESTful APIs that consume a certain percentage of CPU capability or memory amount respetively.



This project is being developed 

Construct an end-to-end solution that deploys two applications to
local machine cloud environment leveraging Infrastructure as Code
technology (e.g. Terraform)
• The applications will be API only and do the following
• Application 1: Detect memory amount of machine running and randomly select
consuming 5/10/15/25/35 percent
• Application 2: Detect CPU capability of machine running and randomly select
consuming 5/10/15/25/35 percent
• Construct performance tests to determine peak usage capabilities
• Construct soak test to determine ensure stability over a period of 10
minutes at peak rate
• Leverage the scaling scenarios to tune the testing models and scaling
strategy for the applications

This project aims to create a chatbot for answering questions related to CSE 332S: Object-oriented software development. This course is offered at WashU as part of the Computer Science and Engineering department and is a required course for all CS majors and minors. The goal of the project is to give students access to a resource for getting help quickly, even if that help may not be perfect. The chatbot will include:

a student facing user interface (likly a web based fron-end), allowing students to submit questions to the chatbot.
a large language model trained on course resources including past piazza posts, course lecture videos, and course recitation recordings.
a RestAPI that connects the user to the chatbot, allowing user questions to be submitted and answers returned.
More details on will be provided regarding each of the above in section 3.
