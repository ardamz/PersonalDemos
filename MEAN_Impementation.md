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
I then went ahead to create a folder named `public`, navigated to the folder and created a file named `script.js`

```bash
mkdir public && cd public
```
```bash
vi script.js
```
![Screenshot](https://github.com/ardamz/PersonalDemos/b)

![Screenshot](https://github.com/ardamz/PersonalDemos/b)
> I poplulated the script.js file as above.










And I ran the following code to verify the Node.js and NPM installation.

```bash
node -v
```
```bash
npm -v
```

![Screenshot](https://github.com/ardamz/PersonalDemos/blob/6e74a7e2b9dc58d5b7df61f3cb8cd8521e6bb662/3.%20Project%203%20MERN%20Stack%20Implementation%20copy/node%20&%20npm%20verification.png)

### *__Application Code setup__*
I created a folder called Todo, navigated into the folder using the `mkdir` and `cd` commands respectively, and initialised my project by running the `npm init` command as shown below

```bash
mkdir Todo
```
```bash
cd Todo
```
```bash
npm init
```

![Screenshot](https://github.com/ardamz/PersonalDemos/blob/6e74a7e2b9dc58d5b7df61f3cb8cd8521e6bb662/3.%20Project%203%20MERN%20Stack%20Implementation%20copy/npm%20initialize.png)

> I followed on screen prompt and pressed enter till the `package.json` file was created.

I ran the `ls` commmand to verify the creation of the package.json file.
![Screenshot](https://github.com/ardamz/PersonalDemos/blob/6e74a7e2b9dc58d5b7df61f3cb8cd8521e6bb662/3.%20Project%203%20MERN%20Stack%20Implementation%20copy/package.json%20confirmed.png) 

### *__Install ExpressJS__*

To install the ExpressJS framework for Node.js

```bash
npm install express
```
![Screenshot](https://github.com/ardamz/PersonalDemos/blob/6e74a7e2b9dc58d5b7df61f3cb8cd8521e6bb662/3.%20Project%203%20MERN%20Stack%20Implementation%20copy/install%20express.png)

After the installation , i created an index.js file using the `touch` command and also used the `ls` command to verify creation of said file.

```bash
touch index.js
```
![Screenshot](https://github.com/ardamz/PersonalDemos/blob/6e74a7e2b9dc58d5b7df61f3cb8cd8521e6bb662/3.%20Project%203%20MERN%20Stack%20Implementation%20copy/touch%20index.png) 


Using the vim text editor, i saved some code in the index.js file as shown below.

```bash
vim index.js
```
```javascript
const express = require('express');
require('dotenv').config();

const app = express();

const port = process.env.PORT || 5000;

app.use((req, res, next) => {
res.header("Access-Control-Allow-Origin", "\*");
res.header("Access-Control-Allow-Headers", "Origin, X-Requested-With, Content-Type, Accept");
next();
});

app.use((req, res, next) => {
res.send('Welcome to Express');
});

app.listen(port, () => {
console.log(`Server running on port ${port}`)
});
```
![Screenshot](https://github.com/ardamz/PersonalDemos/blob/6e74a7e2b9dc58d5b7df61f3cb8cd8521e6bb662/3.%20Project%203%20MERN%20Stack%20Implementation%20copy/vim%20index.js.png)

I tried starting my server by running the `node index.js` command but i got an error of a missing module. Using npm which is the package manager for node i was able to install the missing module, and was ab le to start the server.

```bash
npm install dotenv
```
```bash
node index.js
```
![Screenshot](https://github.com/ardamz/PersonalDemos/blob/6e74a7e2b9dc58d5b7df61f3cb8cd8521e6bb662/3.%20Project%203%20MERN%20Stack%20Implementation%20copy/starting%20the%20server.png)

After seeing that my server was up and running i  decided to verify this using my browser. i used the puublic IP address of the EC2 along with the port number returned earlier.

But for this to work i had to enable the specific port on the EC2 as it is disabled by default for security reasons.

![Screenshot](https://github.com/ardamz/PersonalDemos/blob/111841864814ae5b5e1979c0bdec10f1befa7b96/3.%20Project%203%20MERN%20Stack%20Implementation/SG%20updated.png)

> I got the `Welcome to Express` message in the browser, which verifies that the server is truly working.

![Screenshot](https://github.com/ardamz/PersonalDemos/blob/111841864814ae5b5e1979c0bdec10f1befa7b96/3.%20Project%203%20MERN%20Stack%20Implementation/server%20verified%20in%20browser.png)

### ***Routes***
I will require the Todo app to carry out three tasks,
1. Create a new task,
2. Display list of all tasks and
3. Delete a completed task

Each task will be associated with some particular endpoint and will use different standard HTTP request methods: POST, GET, DELETE.

For each task, I created routes that will define various endpoints that the Todo app will depend on. 

> To achieve this, I ran a sequence of codes to do the following:

1. created a routes folder,
1. navigated to the routes folder,
1. created a api.js file using the `touch` command and
1. saved some lines of code to the the api.js file using `vim`.

```bash
mkdir routes
```
```bash
cd routes
```
```bash
touch api.js
```
```bash
vim api.js
```
![Screenshot](https://github.com/ardamz/PersonalDemos/blob/5473c6bafc11ffd7e213fd528e641132a294b2b5/3.%20Project%203%20MERN%20Stack%20Implementation/create%20routes%20folder.png)
```javascript
const express = require ('express');
const router = express.Router();

router.get('/todos', (req, res, next) => {

});

router.post('/todos', (req, res, next) => {

});

router.delete('/todos/:id', (req, res, next) => {

})

module.exports = router;
```


![Screenshot](https://github.com/ardamz/PersonalDemos/blob/5775b14af80c6a16e1cf1a7f1d7bca3143b13d8a/3.%20Project%203%20MERN%20Stack%20Implementation/api.js%20populated.png)

### ***MODELS***

To create a model that wil be used to define the schema of the mongoDB used for this app, I ran a sequence of codes to do the following:

1. Navigated back to the `Todo` folder.
1. install mongoose using the node package manager.
2. Create a new directory called `models`.
3. Navigate into the new folder, and created a `todo.js` file in the models folder using the  `touch` command.

```bash
cd .. 
```
```bash
npm install mongoose
```
![Screenshot](https://github.com/ardamz/PersonalDemos/blob/5473c6bafc11ffd7e213fd528e641132a294b2b5/3.%20Project%203%20MERN%20Stack%20Implementation/install%20mongoose.png)

```bash
 mkdir models && cd models && touch todo.js
```

![Screenshot](https://github.com/ardamz/PersonalDemos/blob/5473c6bafc11ffd7e213fd528e641132a294b2b5/3.%20Project%203%20MERN%20Stack%20Implementation/create%20models%20folder.png)


Using the vim text editor i saved the code below to the file;
```bash
vim todo.js
```

```javascript
const mongoose = require('mongoose');
const Schema = mongoose.Schema;

//create schema for todo
const TodoSchema = new Schema({
action: {
type: String,
required: [true, 'The todo text field is required']
}
})

//create model for todo
const Todo = mongoose.model('todo', TodoSchema);

module.exports = Todo;
```

![Screenshot](https://github.com/ardamz/PersonalDemos/blob/3eaaf08b1a1b13469665ab2941adf1d482b9d99d/3.%20Project%203%20MERN%20Stack%20Implementation/todo.js%20populated.png)

I then ran the following codes;
 ```bash
cd ~/Todo/routes
```
![Screenshot](https://github.com/ardamz/PersonalDemos/blob/3eaaf08b1a1b13469665ab2941adf1d482b9d99d/3.%20Project%203%20MERN%20Stack%20Implementation/navigate%20to%20routes.png)


> To navigate back to the `routes` folder, and
 ```bash
vim api.js
```
 ```bash
:%d
```
 ```javascript
const express = require ('express');
const router = express.Router();
const Todo = require('../models/todo');

router.get('/todos', (req, res, next) => {

//this will return all the data, exposing only the id and action field to the client
Todo.find({}, 'action')
.then(data => res.json(data))
.catch(next)
});

router.post('/todos', (req, res, next) => {
if(req.body.action){
Todo.create(req.body)
.then(data => res.json(data))
.catch(next)
}else {
res.json({
error: "The input field is empty"
})
}
});

router.delete('/todos/:id', (req, res, next) => {
Todo.findOneAndDelete({"_id": req.params.id})
.then(data => res.json(data))
.catch(next)
})

module.exports = router;
```

![Screenshot](https://github.com/ardamz/PersonalDemos/blob/3eaaf08b1a1b13469665ab2941adf1d482b9d99d/3.%20Project%203%20MERN%20Stack%20Implementation/api.js%20modified.png)

> This was to basically replace the previous content of the `api.js` file using the vim text editor.

### ***MongoDB DATABASE***
I needed a database where my data will be stored. For this, I will make use of [`mLab`](https://www.mongodb.com/atlas-signup-from-mlab). 

After signing up on the platform, I completed a getting started checklist, and in the process I carried out the following;
1. create a DB user and granted permission to the new user.

![Screenshot](https://github.com/ardamz/PersonalDemos/blob/3eaaf08b1a1b13469665ab2941adf1d482b9d99d/3.%20Project%203%20MERN%20Stack%20Implementation/create%20DB%20User.png)

2.  I allowed access to the MongoDB DB from anywhere *(Not ideal/recommended for a prodution enviroment, but it is ideal for testing).*

![Screenshot](https://github.com/ardamz/PersonalDemos/blob/3eaaf08b1a1b13469665ab2941adf1d482b9d99d/3.%20Project%203%20MERN%20Stack%20Implementation/IP%20Access%20List.png)

3. Created a cluster using AWS as my cloud platform.

![Screenshot](https://github.com/ardamz/PersonalDemos/blob/3eaaf08b1a1b13469665ab2941adf1d482b9d99d/3.%20Project%203%20MERN%20Stack%20Implementation/create%20a%20cluster.png)

4. Created a DB and collection.

![Screenshot](https://github.com/ardamz/PersonalDemos/blob/5f8354654739155a4cf26d006387cd40fe979e8f/3.%20Project%203%20MERN%20Stack%20Implementation/Create%20DB%20and%20Collection.png)

5. Accessed my DB connection string by clicking on the `connect` button on the database page.

![Screenshot](https://github.com/ardamz/PersonalDemos/blob/5f8354654739155a4cf26d006387cd40fe979e8f/3.%20Project%203%20MERN%20Stack%20Implementation/get%20.env%20string.png)

I created a `.env` file and saved my DB connection string to it, as a `process.env` was specified in the `index.js` file to access environment variables.

```bash
touch .env
```
![Screenshot](https://github.com/ardamz/PersonalDemos/blob/1ba3d7a3317b564b2de70243c234581914482113/3.%20Project%203%20MERN%20Stack%20Implementation/create%20.env%20file.png)

```bash
vi .env
```
> And the connection string to access the database in it, just as below:

![Screenshot](https://github.com/ardamz/PersonalDemos/blob/1ba3d7a3317b564b2de70243c234581914482113/3.%20Project%203%20MERN%20Stack%20Implementation/latest%20.env%20file.png)

```bash
DB = 'mongodb+srv://ardamz:Password1@mern-stack.7hgerup.mongodb.net/ardamzTestDB?retryWrites=true&w=majority'
```
I then updated the content of the `index.js` file by
1. Running the `vim index.js` command,
1. Pressing the esc button,
1. Typing `:`, followed by
1. Typing `%d` and
1. Hitting the ***Enter*** button.
1. Hit `i` button to enter the insert mode in vim,
1. And finally pasting the entire code block below in the file.

```bash
const express = require('express');
const bodyParser = require('body-parser');
const mongoose = require('mongoose');
const routes = require('./routes/api');
const path = require('path');
require('dotenv').config();

const app = express();

const port = process.env.PORT || 5000;

//connect to the database
mongoose.connect(process.env.DB, { useNewUrlParser: true, useUnifiedTopology: true })
.then(() => console.log(`Database connected successfully`))
.catch(err => console.log(err));

//since mongoose promise is depreciated, we overide it with node's promise
mongoose.Promise = global.Promise;

app.use((req, res, next) => {
res.header("Access-Control-Allow-Origin", "\*");
res.header("Access-Control-Allow-Headers", "Origin, X-Requested-With, Content-Type, Accept");
next();
});

app.use(bodyParser.json());

app.use('/api', routes);

app.use((err, req, res, next) => {
console.log(err);
next();
});

app.listen(port, () => {
console.log(`Server running on port ${port}`)
});
```

![Screenshot](https://github.com/ardamz/PersonalDemos/blob/1ba3d7a3317b564b2de70243c234581914482113/3.%20Project%203%20MERN%20Stack%20Implementation/update%20index.js.png)

8. I then started my server by running the code below, and I got a `Database connected successfully` message as displayed below.

```bash
node index.js
```

![Screenshot](https://github.com/ardamz/PBL/blob/).

### ***Testing Backend Code without Frontend using RESTful API***
Using `Postman`, I tested all the API endpoints to make sure they are working. For the endpoints that required a body, I sent JSON back with the necessary fields since it’s what I will be setting up in my code.


![Screenshot](https://github.com/ardamz/PBL/blob/).

> POST API test finally OK, had some fits with the url, but alls sorted in the end.

![Screenshot](https://github.com/ardamz/PBL/blob/).

>GET API Test Ok, this was quite straight forward.


![Screenshot](https://github.com/ardamz/PBL/blob/).

> DELETE API test finally OK, had to send the request with the id to verify what content to delete.

##  **STEP 2 – FRONTEND CREATION**

I created the user interface (frontend) of my my application using Reactjs. this interacts the DB at the backend using API. navigating to the `Todo` folder of my server, i ran nthe command below.
```bash
npx create-react-app client
```
![Screenshot](https://github.com/ardamz/PBL/blob/).

This created a new folder in my `Todo` directory called client, where all the react code will be added.
![Screenshot](https://github.com/ardamz/PBL/blob/).

### ***Running a React App***
before proceeding, I installed the `concurrently` and `nodemon` dependencies by running;

```bash
npm install concurrently --save-dev
```
![Screenshot](https://github.com/ardamz/PBL/blob/)
> This is used to run more than one command simultaneously from the same terminal window.


```bash
npm install nodemon --save-dev
```
![Screenshot](https://github.com/ardamz/PBL/blob/)
> While this is used to run and monitor the server.

I also edited the package.json file.

![Screenshot](https://github.com/ardamz/PBL/blob/)


![Screenshot](https://github.com/ardamz/PBL/blob/)

I also navigated to the `Todo/client` dirctory and also edited the package.json file by adding the key value pair below,

```
"proxy": "http://localhost:5000"
```
![Screenshot](https://github.com/ardamz/PBL/blob/)


![Screenshot](https://github.com/ardamz/PBL/blob/)

### ***Creating the React Components***

From the `client` directorty, i moved to the src directory and created another directory called `components`, and created three (3) files named `Input.js`, `ListTodo.js` and `Todo.js` in the `components` directory.

![Screenshot](https://github.com/ardamz/PBL/blob/)


![Screenshot](https://github.com/ardamz/PBL/blob/)

Using the nano text editor, i saved the below text to the `Input.js` file.

```bash
import React, { Component } from 'react';
import axios from 'axios';

class Input extends Component {

state = {
action: ""
}

addTodo = () => {
const task = {action: this.state.action}

    if(task.action && task.action.length > 0){
      axios.post('/api/todos', task)
        .then(res => {
          if(res.data){
            this.props.getTodos();
            this.setState({action: ""})
          }
        })
        .catch(err => console.log(err))
    }else {
      console.log('input field required')
    }

}

handleChange = (e) => {
this.setState({
action: e.target.value
})
}

render() {
let { action } = this.state;
return (
<div>
<input type="text" onChange={this.handleChange} value={action} />
<button onClick={this.addTodo}>add todo</button>
</div>
)
}
}

export default Input
```

I then moved back to the `client` directory and installed `axios` which is a Promise based HTTP client for the browser and node.js by running;

```bash
npm install axios
```
After that, moving back to the components directory and using the nano text editor, i saved the below text to the `ListTodo.js` and `Todo.js`  file.

```bash
import React from 'react';

const ListTodo = ({ todos, deleteTodo }) => {

return (
<ul>
{
todos &&
todos.length > 0 ?
(
todos.map(todo => {
return (
<li key={todo._id} onClick={() => deleteTodo(todo._id)}>{todo.action}</li>
)
})
)
:
(
<li>No todo(s) left</li>
)
}
</ul>
)
}

export default ListTodo
```

To make some final adjustment to the view of the front end, i edited the `App.js`, `App.css` and `index.css` file in the `src` directory.vi