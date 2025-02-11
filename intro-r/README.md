# terraform notes 
```
Research Terraform:

    What is Terraform? What is it used for?
    Why use Terraform? The benefits?
    Alternatives to Terraform
    Who is using Terraform in the industry?
    In IaC, what is orchestration? How does Terraform act as "orchestrator"?
    Best practice supplying AWS credentials to Terraform
        If Terraform needs AWS access, there are different options on supplying the AWS credentials to Terraform. What is order in which Terraform looks up AWS credentials (which ways take precedence/priority)?
        What is best practice to supply AWS credentials? Include: How should AWS credentials never be passed to Terraform?
    Why use Terraform for different environments (e.g. production, testing, etc)
``` 

## What is Terraform?
* Terraform is a tool that helps automate infrastructure tasks, such as provisioning cloud resources. It's an open-source, cloud-agnostic tool written in the Go language
### What it's used for 

* Automating infrastructure provisioning in cloud and on-premises environments
* Provisioning cloud resources
* Managing infrastructure in multi-cloud and hybrid environments 

## Why use Terraform? The benefits?
* centralised management 
* automated workflow
* version control  
* portable 
* quick to deploy 
* built in security 


## Who is using Terraform in the industry?
* Oracle
* EPAM Systems
* Intellibus
* Deloitte

## In IaC, what is orchestration? How does Terraform act as "orchestrator"? 
In Infrastructure as Code (IaC), "orchestration" refers to the process of coordinating and managing multiple complex infrastructure components across different cloud providers, ensuring they are deployed and configured in the correct order and dependencies are met

## Best practice supplying AWS credentials to Terraform 
* dont hardcode credentials
* use IAM rules 
* set environment variables

## infrastructure as code (IaC)
* configuration management i.e. ansible
* orchestration tool ie terraform 

### orchestration 
* directing the infrastructure
  *  what runs where 
  *  can make instances 
  *  infrastructure also has dependancys and terraform can be used to set these up in the correct order 
  *  decides on lifecycle of infrastructure 
  *  terraform views infrastructure as immutable, hence have to destroy and remake 
  *  terraform is declarative
### configuration 
* ansible is very good at changing the setup of infrastructure, not orchestrating 
* ansible is imperitive 
## idempotent 
* idempotent - always ends up in desired state, no matter how many times something is run 

## IaC 
* prevent configuration drift 
  * changing of configurations on different servers, so they end up being different, which can break things down the line 
  * configuration management tools like terraform can prevent this drift and keep things standardised 
  * where as a tool like terraform will state the ideal configuration 


# terraform commands 

- terraform init: Used to initialize a working directory containing Terraform config files and to download providers and modules.
- terraform validate: Validates the Terraform config in that particular directory to ensure they are syntactically valid and internally consistent.
- terraform plan: Creates an execution plan. Using this command prompts Terraform to perform a refresh and determine the actions necessary to achieve the desired - state in specified config files.
- terraform apply: Used to apply the changes required to reach the desired configuration state. By default, the apply command scans the current directory for the - config and applies the changes appropriately.