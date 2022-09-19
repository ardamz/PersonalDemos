# MEAN means MongoDB ExpressJS Angular & Node.JS


<!-- I utilised AWS EC2 as my Linux portion of the stack. I used an Ubuntu 20.04 LTS server, any Linux distro would equally work.!-->

To update the OS repositories, I ran the following codes

```bash
sudo apt update
```
![Screenshot](https://github.com/ardamz/PersonalDemos/blob/6e74a7e2b9dc58d5b7df61f3cb8cd8521e6bb662/3.%20Project%203%20MERN%20Stack%20Implementation%20copy/Update.png)

To upgrade the OS, I ran the following codes

```bash
sudo apt upgrade
```
![Screenshot](https://github.com/ardamz/PersonalDemos/blob/6e74a7e2b9dc58d5b7df61f3cb8cd8521e6bb662/3.%20Project%203%20MERN%20Stack%20Implementation%20copy/Upgrade.png)

### *__Step 1 -  Node.js Installation.__*

To Install the Node.js software, I ran the following codes


```bash
sudo apt -y install curl dirmngr apt-transport-https lsb-release ca-certificates

curl -sL https://deb.nodesource.com/setup_18.x | sudo -E bash -
```

![Screenshot](https://github.com/ardamz/PersonalDemos/blob/6e74a7e2b9dc58d5b7df61f3cb8cd8521e6bb662/3.%20Project%203%20MERN%20Stack%20Implementation%20copy/locate%20nodejs.png)

> To add certificates, and

```bash
sudo apt install -y nodejs
```
> To install Node.js software.

![Screenshot](https://github.com/ardamz/PersonalDemos/blob/6e74a7e2b9dc58d5b7df61f3cb8cd8521e6bb662/3.%20Project%203%20MERN%20Stack%20Implementation%20copy/install%20nodejs%20&%20npm.png)

### *__Step 2 -  MongoDB Installation.__*

I installed the MongoDB by running the following code;


```bash
sudo apt install -y mongodb-org
```
> The procedures followed can be found [here](https://www.cherryservers.com/blog/how-to-install-and-start-using-mongodb-on-ubuntu-20-04)

```bash
mongod --version
```
> I ran this to verify the MongoDB installation.

I then proceeded to start the server, and verify same by running the following codes

```bash
sudo service mongod start
```

```bash
sudo systemctl status mongod
```

![Screenshot](https://github.com/ardamz/PersonalDemos/b)


#### Install npm – Node package manager.

```bash
sudo apt install -y npm
```
To install body-parser package, run

```bash
sudo npm install body-parser
```

I then went ahead to create a folder named `Books`, navigate to the `Books` directory and initialized an npm project by running the folowing commands;

```bash
mkdir Books && cd Books
```
```bash
npm init
```

I added a file to the directory named `server.js` 

```bash
vi server.js
```
![Screenshot](https://github.com/ardamz/PersonalDemos/b)

![Screenshot](https://github.com/ardamz/PersonalDemos/b)

> Popluated the `server.js` file as above.


### *__Step 3 - Install Express and set up routes to the server.__*

Mongoose is a package which provides a straight-forward, schema-based solution to model our application data. I will use Mongoose to establish a schema for the database to store data of our book register.

```bash
sudo npm install express mongoose
```
> I ran the above command to insatll mongoose.

From the `Books` folder, I created a folder named `apps`, and created a `routes.js` file in this new directory by running the following commands.

```bash
mkdir apps && cd apps
```
![Screenshot](https://github.com/ardamz/PersonalDemos/b)

```bash
vi routes.js
```
![Screenshot](https://github.com/ardamz/PersonalDemos/b)
> I poplulated the routes.js file as above.

From the `apps` folder, I created a folder named `models`, navigated to the folder and created a `books.js` file by running the following commandss;

```bash
mkdir models && cd models
```
![Screenshot](https://github.com/ardamz/PersonalDemos/b)

```bash
vi book.js
```
![Screenshot](https://github.com/ardamz/PersonalDemos/b)
> I poplulated the books.js file as above.

### *__Step 4 – Access the routes with AngularJS.__*
> AngularJS provides a web framework for creating dynamic views in  web applications. In this project, I made use of AngularJS to connect my web page with Express and perform actions on my book register.

I navigated to the `books` directory by running the command below.
```bash
cd ~/Books
```
I then went ahead to create a folder named `public`, navigated to the folder, created and populated a file named `script.js` with some lines of code using the `vi` command.

```bash
mkdir public && cd public
```
```bash
vi script.js
```
![Screenshot](https://github.com/ardamz/PersonalDemos/b)

![Screenshot](https://github.com/ardamz/PersonalDemos/b)
> I poplulated the script.js file as above.

In the same `public` folder, I also created and populated an  `index.html` file with some lines of code using the `vi` command.

```bash
vi index.html
```
![Screenshot](https://github.com/ardamz/PersonalDemos/b)

![Screenshot](https://github.com/ardamz/PersonalDemos/b)
> I poplulated the index.html file as above.

I navigated back to the `Books` folder, and started the server by running the following commands.

```bash
cd ..
```
> To navigate to the Books folder.

```bash
node server.js
```
>To start the server.


![Screenshot](https://github.com/ardamz/PersonalDemos/b)

Running the `curl -s http://localhost:3300` returned the content of the `index.html` to my terminal screen as shown by the image below.
![Screenshot](https://github.com/ardamz/PersonalDemos/b)

I also verified the status of the server by visiting the public IP address of my server, and i was able access and interact with my Web Book Register APplication as shown by the pix below.
![Screenshot](https://github.com/ardamz/PersonalDemos/b)
>Before populating my DB

![Screenshot](https://github.com/ardamz/PersonalDemos/b)
>After populating my DB.







