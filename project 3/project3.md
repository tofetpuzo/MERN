# MERN STACK IMPLEMENTATION
The MERN stack is a web framework which delivers powerful results simply and efficiently especially when the goal is to build sophisticated web applications.

The process of implementing this framework is explained. The first process is connect my local terminal to aws Ubuntu server using the EC2 instance, I will be using the bash terminal for all the configuration and implementation.

The first step is update and upgrade Ubuntu using this line of code

`:~ $ sudo apt update && sudo apt upgrade`

After this step, I went on to get the location of Node.js software from Ubuntu repositories, using this command:

`:~ $ curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -`

The next step is to install Node.js after obtaining the key, this was done with this code: 

`:~ $ sudo apt-get install -y nodejs`

I verified that node.js is running, screenshot below.

![node](./images/update.png)

I also verified that npm was also correctly installed.
![node](./images/npm.png)

Now that I have confirmed that the node.js is installed, I then proceed to initialize my project, using this code:

`:~ $ npm init` 
 
 This will allow a package.json file to be created. The file contains information about the application and dependencies required for applications to run smoothly.

 ![node](./images/ins.png)


 ## Installing Express
 ___
 
The next step is to install express which is a framework used in node.js and create an index file. To do this i used the commands below:

`:~ $ npm install express` 

`:~ $ touch index.js`

After this I went on to install dotenv which is just a dependency file used to store variables in an application environment. I used this command:
 
`:~ $ npm install dotenv`

 When this was done, I went on to edit the index.js file earlier created and wrote code which will be used to configure the Server. I used port 3000 for communication port between app and server.

`:~ $ nano index.js`

 ![node](./images/ser.png)

 After running this , I ran this command to check if the server will be listening on 3000.


`:~ $ node index.js`

The screenshot is below
![express](./images/expressworks.png)

After making sure that my Todo app has been successfully configured to listen on a port in the server, I went on to create a routes folder; this folder contains what the app will do like get, post and delete. A file called the api.js was created and the code that will be used to execute those functions were placed in the file. 

`:~ $ mkdir routes`

`:~ $ cd routes`

`:~ $ touch api.js`

The next step is to create a model; this is usually considered the heart of JavaScript which is used to make the Todo app more interactive.


 ### Creating a Schema and a model
 ___
After which I install mongoose using the command:

`:~ $ npm install mongoose`

The mongoose makes working with node.js easier. Now the interesting part is to is to create a directory called models, and create a file called todo.js. I used this line of code to execute these aforementioned steps.

`:~ $ mkdir models && cd models && touch todo.js`

After which i did edited the api.js which now contains the router information such as get, delete and post. 

 ## Configuring MongoDB
 ___ 

To store information in the todo app, I need a database: MongoDB. This database is a non-relational database. The next step is to create a MongoDB database and collection inside mLab, usually called Cluster. 

![MDB](./images/mongo.png)

Now that I have a working database, I then proceed to create an .env file: This file contains information about the MongDB credentials.
The next step is to edit to index.js file to reflect the .env file which will be used by node.js to connect to the MongoDB.

The use of environment variables to store information was solely done in other to secure the configuration and secret data for the application, as against writing connection strings directly to the index.js file.

After this configuration, I ran the file to see if the database did run successfully configured.

![MDB](./images/database.png)


 ## Using Postman
 ___ 

Now that I have configured my backend , I intend to use ReactJS code to achieve this. But before doing this, it is important to test code using RESTful API. I used postman to create a POST request; this sends request to the server, and the server in turn calls on the database to fetch the requested data. I also certain if I could use the GET and DELETE request. The Screenshots below:

The Post request:

![po](./images/s1.png)

![po1](./images/s2.png)



The GET Request successfully executed

![po2](./images/s3.png)



The DELETE request was executed successfully using the 
id produced by Postman.



![po3](./images/s4.png)




After the DELETE Request, I used the GET request to test if the DELETE request was executed. Screenshot below:

![po4](./images/s5.png)

 ## Creating Frontend Application
 ___ 

After successfully configuring the backend API, The next step is to create a user interface for Web client to interact via the API. 

The first step is to use the create-react-app command to scaffold our app:


`:~ $  npx create-react-app client`


Second step was to install concurrently, this is used to run more than one command simultaneously , I did this using the command. :

`:~ $  npm install concurrently --save-dev`

The next step is to install nodemon, It is used to run and monitor the server. If there be any changes committed , nodemon will automatically load the changes. To do this I used this command:

`:~ $  npm install nodemon --save-dev`

After this, I changed directory to package.json where I inserted code to specified a no error test and integrated concurrently. To configure the client I changed the directory and edited the package.json file from there adding the value pair key into it. I following commands were used.

`:~ $  cd client`

`:~ $  vi package.json`

// Add key value pair. The main reason for this is to have access to the application directly through the browser.
"proxy": "http://localhost:5000".

To run the application, I used this command below, this allows it run on localhost using port range 3000.

 ## Creating React Components
 ___ 

The next step is to the create react components; one of the advantages of using react is that , the components are reusable and also makes code modular.

To create the components below are the line of code used:

`:~ $  cd client`

`:~ $  cd src`

`:~ $  mkdir components`

`:~ $  cd components`

The following code was used to create different files which was used to code.

`:~ $  touch Input.js ListTodo.js Todo.js`

For each of this file , I wrote lines of code to build the application. Now that I have successfully 
