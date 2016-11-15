# HW1 - Provisioning and Configuring Servers

Name: Shivam Gulati

Email: sgulati2@ncsu.edu

This demonstrates server provisioning and configuration on below 2 providers:

1. Digital Ocean
2. AWS 

[AWS Paragraph](https://github.ncsu.edu/sgulati2/HW1#about-aws)

#### Digital Ocean

1. Create a Digital Ocean account if not existing already. Login to the account.
2. Under the API tab, create an API token. Save the token somewhere for record since you won't be able to see it later.
3. Generate public and private keys using keygen.
4. Pass the token to do.js file which provisions droplet and writes the inventory file to be consumed by ansible.

```
node do.js
```

#### AWS

1. Create a AWS account if not existing already. Login to the account.
2. Create access_key_id and secret_access_key from Security Credentials.
3. Pass the secret access key in code or setup a credentials file in machine.
3. Generate public and private keys using keygen and import keypair in AWS. 
4. Create a security group. Edit its inbound attribute for SSH permissions. Pass them to parameters in script.
5. Run aws.js file which provisions server and writes the inventory file to be consumed by ansible.

```
node aws.js
```

#### Ansible Playbook

1. Make sure you have ansible installed and configured. If not, follow [Ansible Configuration](https://github.com/CSC-DevOps/Course/blob/master/Workshops/CM.md#configuration-with-ansible)
2. Create ansible playbook file to setup nginx webserver.
3. To run the same 

```
ansible-playbook ansibleplay.yml -i inventory
```

where ansibleplay.yml is the name of file created

#### Configuration management

1. All dependencies are in package.json file.
2. To build using npm, go to the project folder and run the below command

```
npm install
```

### About AWS

Amazon EC2(Elastic Compute Cloud) provides resizable cloud computing capacity. Developers use for scalable cloud computing applications.

Developers can use AWS APIs provided in different languages to leverage and utilize computing services for their applications. It greatly reduces the server server provisioning and configuration time for developers to quickly put up their services on the web. On the flipside, it takes a lot of time to manually setup a server and making it scalable and maintainable is a big pain. Developers pay for the services as per their usage.

AWS services are managed through user account on AWS console. Users can login and setup the services they need. eg. EC2 APIs easily allow to setup and manage server instances to be utlized for computing. Similary for other storage solutions, analytics, management tools, etc.

Sources:

1. https://en.wikipedia.org/wiki/Amazon_Web_Services
2. http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/concepts.html
3. https://aws.amazon.com/documentation/gettingstarted

#### Screencast

![Screencast](https://github.com/shivamgulati1991/HW1-ConfigureServers/blob/master/HW1_sgulati2.gif)

[Link to GIF] (https://github.com/shivamgulati1991/HW1-ConfigureServers/blob/master/HW1_sgulati2.gif)
