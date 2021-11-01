# MERN STACK IMPLEMENTATION
The MERN stack is a web framework which delivers powerful results simply and efficiently especially when the goal is to build sophisticated web applications.

The process of implementing this framework is explained. The first process is connect my local terminal to aws Ubuntu server using the EC2 instance, I will be using the bash terminal for all the configuration and implementation.

The first step is update and upgrade Ubuntu using this line of code

`sudo apt update && sudo apt upgrade`

After this step, I went on to get the location of Node.js software from Ubuntu repositories, using this command:

`curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -`

The next step is to install Node.js after obtaining the key, this was done with this code: 

`sudo apt-get install -y nodejs`

I verified that node.js is running, screenshot below.

![node](./images/update.png)

I also verified that npm was also correctly installed.
![node](./images/npm.png)

Now that I have confirmed that the node.js is installed, I then proceed to initialize my project, using the npm init. This will allow a package.json file to be created. This file contains information about the application and dependencies required for applications to run smoothly 