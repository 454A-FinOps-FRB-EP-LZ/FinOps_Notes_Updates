# FinOps E2E Semester plan - How will your team work?

## An overview of technologies used to develop your solution and how your team will work:

### How will you maintain and store the code (github, bitbucket, local storage, wustl box, etc.):
To store our source code, we have created a GitHub organization where we are making repositories for each component of our project, such as the REST APIs, the AWS EC2 instance for hosting the REST APIs and the AWS EC2 cluster which we are going to implement and test the scaling rules.

### What tools will you use to track your development/progress? (Trello, github projects, a written document are all possibilities):
To track our development progress, we are going to be using GitHub projects to keep track of the completion of the different tasks we are setting for each month.

### Frameworks an programming languages used:
The frameworks we are going to be using are the AWS CLI, GitLab, Terraform, AWS EC2 instances, the AWS SSM (Systems Manager) and the Python Flask library.

The langages we are going to be using are Python and HCL (HashiCorp Configuration Language) which is a language for terraform and is similar to JSON.

### How will the software be deployed?
The software will be deployed to an EC2 instance via AWS SSM and GitLab.

### Other processes required
Learning more about EC2 instances and how to define base security, networking and permission capabilities to grant access into the instance via SSM without a key pair.

### How you will test your product?
We will test our APIs via load and soak tests which test for scalability and stability respectively. We will test the ability of our EC2 clusters to scale via the auto scaling rules by the random CPU and memory assignments done with the two APIs.
