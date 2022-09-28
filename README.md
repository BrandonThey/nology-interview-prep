## Cloud & DevOps
### Explanation
Cloud and DevOps to me is the process of taking a product from the start to finish, incrementally. 
From actually code and creating an app, to building pipeline and deploying the app to the Cloud.

### Experience
I believe that the best example of this concept is my team's final project at Nology. 
In the project we were tasked to create a profile uploader, the idea being that a user can upload profiles that would be saved onto a MySQL database, and hosting that application on AWS. 
A more in-depth look into the project would show us creating a front-end website built using React that allows the user to upload, download, and group profiles. 
The upload and download features are linked to the back-end api and MySql database. 
This back-end creates two tables, one to contain profile information, another to contain user information. 
We get profiles from the front-end and data about the profile then store the profile file into a AWS S3 bucket, which returns us a link to that location to be stored in the MySQL database. 
We also use Terraform to orchestrate our AWS infrastructure and Jenkins as our pipeline to the infrastructure.

### Benefits
The benefits of the Cloud in general and DevOps are vast. 
Using the DevOps cycle, teams can take their project from start to finish which allows for faster and better product delivery, faster issue resolution and reduced complexity from passing the work onto others. However, the greatest benefit is the automation of most of the process, pipelines, infrastructure, and deployment can all be automated to reduce time spent on them and improve resource utilzation.

## CICD
### Explanation
Of course, with agile the DevOps process is done incrementally and that's where the idea of CICD come in. 
CICD is the process of frequently devoloping and integrating functionality into the application through the use of automation. 
A lot of concepts and benefits of CICD are similar to those of DevOps, as they're closely related.

### Experience
Since DevOps and CICD are closely related, I believe that the best example of this is my team project once again. 
In the project we used Terraform to orchestrate our AWS infrastructure and Jenkins to automate our pipeline to the AWS infrstructure. 
Terraform allowed us to easily create our AWS vpc, and subsequently our subnets to host both our application and api/database. 
The Jenkins pipeline was set so that every time a merge happened to our Github main branch, it would build on Jenkins and if the build was successful, the build would be deployed on the AWS E2 instances. 

### Benefits
Reading how CICD worked in our team project really proves how useful CICD and automation is. 
The team could easily create AWS infrastructure and easily deploy our application onto it rather than having to do the steps manually taking more time and resources.

## Jenkins
### Explanation
Jenkins is a tool that helps set up a CICD environment by creating piplines between repositories while also allowing developers to automate routine tasks. 

### Experience
Going back to my team project, I had mentioned that we used a Jenkins pipeline to deploy our application onto the AWS infrastructure.
Well really we had created two pipelines, one for the front-end React application and one for the NodeJS api and MySQL database backend.
These pipeline were linked to each respective Github repository so that every time a merge to the main branch occured the build would run and if successful, would deploy to the AWS instances.  

### Benefits
There are many benefits of Using Jenkins, of course there's the pipelines mentioned earlier allowing programs to be pipelined to any other repository. 
This pipeline is also flexible, allowing the developers to add steps to it before deploying. 
For example, adding testing to the pipeline so that your application may only deploy if your testing is successful. 
There's also the benefit of automation, not only does this save time for the developer, but it also helps to eliminate user error and minimizes the effects of differing environments.

## Provisioning
### Explanation
Provisioning is the process of setting up infrastructure after it has been created.
Often times it is seen as configuring, but the two are different.
While they both share the same functionality, provisioning is the initialization of the resource while configuration is the changing of those settings. All that to say, provisioning comes first. 
Provisioning works in all different ways depending on what resource you're setting up.
A basic virtual machine provisioning might include pre-installing dependencies or even running the application in its entirety. 

### Experience
Using the concept of provisioning, I took a simple Python text game and deployed it to a local virtual machine. 
This was done by using Vagrant, a tool used for building virtual machines. 
In my Vagrantfile there are configurations to create a virtual machine, then there is section to run a basic provisioning script.
In said script, there are shell commands for a unix enviroment that update the enviroment, install python, move into the app folder and start the game. Provisioning is as simple as that. 

### Benefits
The benefits of provisioning are apparent, the ability to set up a resource ahead of time is invaluable. Not only can a developer easily prepare an enviroment for use, but the script itself can eliminate human error during setup and allows for easy transfer of script files.

## Networking
### Explanation
Networking is the connection between different devices where information can be passed between the devices. When it comes to AWS and software development it really means how can a user or a developer connect to a application that hosted remotely. 

### Experience
I previously mentioned hosting a python game on a virtual machine using Vagrant. 
Along the same lines is hosting a React front-end application and an api/database in a seperate machine.
I think hosting these two applications in seperate machines and connecting them together was one of the more difficult yet rewarding obstacles I've encountered. 
In order to accomplish this, each machine must have their own ip address and ports that can be accessed by outside sources.
Then using those ip addresses and ports we can easily connect the machines.

### Benefits
Obviously the immediate benefit of networking is being able to connect to any Cloud infrastructure. 
Then there are the smaller details of networking such as being able to limit who can or cannot access your application or machine. 
In a world that's very connected by the web, its important to protect your application from outside influences.

## Principle of Least Privilege
### Explanation
The Principle of Least Privilege is the concept that someone or something should only have the minimum amount of privileges needed to complete the tasks. 
This is to help minimize the risk of attacks on the application as well as to help contain any damange that an attack may cause.

### Experience
In the team project, we decided that a user of the profile uploader should have the least amount of privileges. T
his is to limit any malicious actors from uploading or downloading files that they should not have access to. 
Even worse, to prevent any malicious actors from changing other user privileges. 
In fact we've limited the way that a user is created, instead of giving people the ability to make their own profile, we decided that an admin can only add new users.
This is so that admin can assign privileges to the user on creation, and to prevent the creation of a new user that lacks all privileges. 

### Benefits
A lot of benefits are self-explanatory when it comes to privileges. 
One benefit is to minimize the chance of attacks to an application,
the less high level accounts there are, the less damage there is.
Another benefit being the prevention of human error, 
if anyone in an organization can make big changes then it's a lot more likely to have human errors in the application.
The last large benefit is one I've mentioned, protecting data.
There may information that low level users should not be able to access, for example SSN, credit-card information, address, etc.

## IAC
### Explanation
Infrastructure as code is the concept of creating infrastructure such as virtual machines or databases using code over manually creating those resources.
With IAC you create configuration files that contain the settings for your infrastructure which will allow a developer to automate the process as well as removing human error.

### Experience
In our team project, we orchestrate all our infrastructure using Terraform and Packer, which in turn means that we don't have to manually go onto AWS and create that infrastructure. Terraform was used to create our vpc, subnets, gateways, and EC2 instances on AWS, along with create a database on the EC2 instance for the backend. Packer was used to create an ami from our existing local virtual machines to be used as a sort of blueprint for the AWS instances.

### Benefits
Much like the rest of the concepts previously discussed, IAC has many benefits in cost reduction, reduced build times, simplified builds and reduced likelihood of errors

## Packer and Terraform
### Explanation
### Experience
### Benefits

