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

