# nology-interview-prep
## Cloud & DevOps
### Explanation
Cloud and DevOps to me is the process of taking a product from the start to finish, incrementally. 
From actually code and creating an app, to building pipeline and deploying the app to the Cloud.
---
### Experience
I believe that the best example of this concept is my team's final project at Nology. 
In the project we were tasked to create a profile uploader, the idea being that a user can upload profiles that would be saved onto a MySQL database, and hosting that application on AWS. 
A more in-depth look into the project would show us creating a front-end website built using React that allows the user to upload, download, and group profiles. 
The upload and download features are linked to the back-end api and MySql database. 
This back-end creates two tables, one to contain profile information, another to contain user information. 
We get profiles from the front-end and data about the profile then store the profile file into a AWS S3 bucket, which returns us a link to that location to be stored in the MySQL database. 
We also use Terraform to orchestrate our AWS infrastructure and Jenkins as our pipeline to the infrastructure.
---
### Benefits
The benefits of the Cloud in general and DevOps are vast. 
Using the DevOps cycle, teams can take their project from start to finish which allows for faster and better product delivery, faster issue resolution and reduced complexity from passing the work onto others. However, the greatest benefit is the automation of most of the process, pipelines, infrastructure, and deployment can all be automated to reduce time spent on them and improve resource utilzation.

## CICD
### Explanation
Of course, with agile the DevOps process is done incrementally and that's where the idea of CICD come in. 
CICD is the process of frequently devoloping and integrating functionality into the application through the use of automation. 
A lot of concepts and benefits of CICD are similar to those of DevOps, as they're closely related.
---
### Experience
Since DevOps and CICD are closely related, I believe that the best example of this is my team project once again. 
In the project we used Terraform to orchestrate our AWS infrastructure and Jenkins to automate our pipeline to the AWS infrstructure. 
Terraform allowed us to easily create our AWS vpc, and subsequently our subnets to host both our application and api/database. 
The Jenkins pipeline was set so that every time a merge happened to our Github main branch, it would build on Jenkins and if the build was successful, the build would be deployed on the AWS E2 instances. 
---
### Benefits
Reading how CICD worked in our team project really proves how useful CICD and automation is. 
The team could easily create AWS infrastructure and easily deploy our application onto it rather than having to do the steps manually taking more time and resources.

## Jenkins
    Jenkins is a tool that helps set up a CICD environment by creating piplines between repositories while also allowing developers to automate routine tasks. 
    ---
    Going back to my team project, I had mentioned that we used a Jenkins pipeline to deploy our application onto the AWS infrastructure.
    Well really we had created two pipelines, one for the front-end React application and one for the NodeJS api and MySQL database backend.
    These pipeline were linked to each respective Github repository so that every time a merge to the main branch occured the build would run and if successful, would deploy to the AWS instances.  
    ---
    There are many benefits of Using Jenkins, of course there's the pipelines mentioned earlier allowing programs to be pipelined to any other repository. 
    This pipeline is also flexible, allowing the developers to add steps to it before deploying. 
    For example, adding testing to the pipeline so that your application may only deploy if your testing is successful. 
    There's also the benefit of automation, not only does this save time for the developer, but it also helps to eliminate user error and minimizes the effects of differing environments.

## Provisioning
    Provisioning is the process of setting up infrastructure after it has been created.
    Often times it is seen as configuring, but the two are different.
    While they both share the same functionality, provisioning is the initialization of the resource while configuration is the changing of those settings. All that to say, provisioning comes first. 
    Provisioning works in all different ways depending on what resource you're setting up.
    A basic virtual machine provisioning might include pre-installing dependencies or even running the application in its entirety. 
    ---
    Using the concept of provisioning, I took a simple Python text game and deployed it to a local virtual machine. 
    This was done by using Vagrant, a tool used for building virtual machines. 
    In my Vagrantfile there are configurations to create a virtual machine, then there is section to run a basic provisioning script.
    In said script, there are shell commands for a unix enviroment that update the enviroment, install python, move into the app folder and start the game. Provisioning is as simple as that. 
    ---
    The benefits of provisioning are apparent, the ability to set up a resource ahead of time is invaluable. Not only can a developer easily prepare an enviroment for use, but the script itself can eliminate human error during setup and allows for easy transfer of script files.
## Networking
    ---
    ---

## Principle of Least Privilege
    ---
    ---


## IAC
    ---
    ---


## Packer and Terraform
    ---
    ---

