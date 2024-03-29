# Small Introduction On Stack
What is a Technology stack?
A technology stack is a set of frameworks and tools used to develop a software product. This set of frameworks and tools are very 
specifically chosen to work together in creating a well-functioning software. They are acronymns for individual technologies used
together for a specific technology product. some examples are…

- LAMP (Linux, Apache, MySQL, PHP or Python, or Perl)
- LEMP (Linux, Nginx, MySQL, PHP or Python, or Perl)
- MERN (MongoDB, ExpressJS, ReactJS, NodeJS)
- MEAN (MongoDB, ExpressJS, AngularJS, NodeJS
# Step 0 – Preparing prerequisites
In order to complete this project you will need an AWS account and a virtual server with Ubuntu Server OS.

[AWS](https://aws.amazon.com/) is the biggest Cloud Service Provider and it offers a free tier account that we are going to leverage for our projects.

Do not focus too much on AWS itself right now, there will be a proper Cloud introduction and configuration projects later in our course.

Right now, all we need to know is that AWS can provide us with a free virtual server called EC2 (Elastic Compute Cloud) for our needs.

Spinning up a new EC2 instance (an instance of a virtual server) is only a matter of a few clicks.

You can either Watch the videos below to get yourself set up.

1. AWS account setup and Provisioning an Ubuntu Server
2. Connecting to your EC2 Instance

Or follow the instructions below.

1. Register a new AWS account following this instruction.
2. Select your preferred region (the closest to you) and launch a new EC2 instance of t2.micro family with Ubuntu Server 20.04 LTS (HVM)
launch EC2

IMPORTANT – save your private key (.pem file) securely and do not share it with anyone! If you lose it, you will not be able to
connect to your server ever again!

For Windows users, you will need a tool called putty to connect to your EC2 Instance. Download Putty Here: https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html.
For Mac users, you can simply open up Terminal and use the ssh command to get into the server.

IMPORTANT NOTICE
Both Putty and ssh use the SSH protocol to establish connectivity between computers. It is the most secure protocol because it uses
crypto algorithms to encrypt the data that is transmitted – it uses TCP port 22 which is open for all newly created EC2 intances in
AWS by default. Most of these terminologies will make more sense to you as you proceed. So for now, if nothing makes sense, just 
ignore. But be assured that the information is already registered in your sub-conscious mind. So it will become useful to you soon.

![projject1-step0](https://user-images.githubusercontent.com/85270361/210112007-5cd14a18-8aaa-4c7a-857e-b18400535bdd.PNG)


