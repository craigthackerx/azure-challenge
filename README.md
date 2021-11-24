# azure-challenge

Welcome to the Azure challenge.  This challenge is intended to test your basic compentency within a typical Cloud and DevOps based scenario.  While it is possible to complete this project and implement a fully functional and complete product, the intention is to give you experience with a full-stack type system development and deployment.

For this, I recommend you sign up for a Free Azure Account and get Azure credits.  I also recomend using Azure free tier for all resources.  

All of these challenges can be attempted in any order you wish, and attempting one before another could be considered more optimal depending on your solution/

Working solutions to all of these challenges can be provided by myself direct, please get in contact via https://craigthacker.dev

Now to get into the challenge:

## Challenge 1: Designing Tenancy Administrative control

For this, you are expected to implement and document how you would add the following users, roles and subscriptions to an Azure AD tenant. Please consider the least privilege and good implementation of automation for future repeatability:

- Create 5 new users (not guest users) in your tenant with the following roles:
   - Craig Thacker - Global Administrator
   - Charlie Johnstone - Global Reader
   - Alan Rae - User Access Administrator
   - Dennis Ritchie - Cloud Device Administrator
   - Lionel Messi - Custom role, with the ability to turn Virtual machines on or off, but not have the ability to create or delete.


- Create 3 subscriptions:
  - CyberScot-Hw-Prd
  - CyberScot-Hw-Mvp
  - CyberScot-Hw-Stg


- You need to add the following IAM access to these subscriptions:
  - The user "Craig Thacker" needs to be able to manage the CyberScot-Prd and HelloWorld-Prd subscritpion, but only read HelloWorld-Mvp
  - Charlie Johnstone must be able to manage everything except other people's permissons on all subscriptions
  - Lionel Messi must be able to start and stop VMs in all subscriptions, but nothing else

Please note there is more than one way to achieve this, and you are being scored purely on your thought process on this and how you would document it. You should include screenshots and examples of your work.


## Challenge 2: Automation Tool Challenge

For this challenge, you need to setup an automation tool to run pipelines  and CI/CD on. This tool should have the latest version of Python3 with `pip`, latest Terraform installed and the ability to build OCI or Docker containers.  This can be a hosted tool such as GitHub Actions, Azure Devops or GitLab or a local hosted solution such as Jenkins.  You then must then create a pipeline which will output "Hello World!" to the terminal.  How you do this is your choice.

I would suggest using Azure DevOps or GitHub Actions, but again, this is open to interpretation for the engineer to provide a sufficient solution.

Please consider least privilege and proper security controls when setting this up.  Ensure sufficient documentation is available on your steps.

## Challenge 2: Terraform Challenge

With terraform, provison an environment similar to that which follows:

1. You should allow for sufficent security control inside your system - this does not require the full implementation of endpoint protection, but should consider the process of "least priviledge"
2. 