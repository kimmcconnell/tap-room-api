# Tap Room API
#### Express / Knex / MySQL back end for tap-room-react project (api branch)
_Published_ **April 21 2019**<br>
_Author_  **Kimberly McConnell**
<hr/>

## **Set Up Guide**
_This guide will tell you how to set this project up for yourself. It assumes you have brew installed._
***

### **Create a project directory**
Create and initalize a directory to hold Express

```bash
$ mkdir test-project
$ cd test-project
$ npm init
```
_This will promt you with some questions. In my project, I used app.js as the entry point, but the basic configuration is fine too._

### **Install Express**
Express is a minimalist web application framework for Node.js. It provides functionality ("middlewear") to handle and respond to http requests, define routing, and more. 

```bash
$ npm install express --save
```

**Hello World with Express**

_This code comes from the [Express Getting Started](https://expressjs.com/en/starter/hello-world.html) guide on the Express website_

Open up your entry point file (app.js, or index.js if you went with the default) in your favorite text editor and enter the following code:
```javascript
const express = require('express')
const app = express()
const port = 3000

app.get('/', (req, res) => res.send('Hello World!'))

app.listen(port, () => console.log(`Example app listening on port ${port}!`))
```
We're got two different functions here, a get and a listen. <br/>
If you navigate to http://localhost:3000 in your browser, you should see the resonse of the get request, your hello world message! <br/>
In your terminal, run 
```bash
$ node app.js
```
and you'll see the response of the listen! _Note: If you used a different entry-point filename, use that here._

###  **Setting up MySQL**
MySQL is an SQL database management system. It is a relational database, so all data is structured in defined tables.

From anywhere on your computer, run:
```bash
$ brew install mysql
```
Because brew is installing MySQL in `usr/local/Cellar`. If you want to check that it's there, run the following:
```bash
$ ls usr/local/Cellar
```

Great! Now that we have MySQL, we can start running it with 
```bash
$ mysql -u root
```
`-u` refers to the user, and `root` is the default user.


### **Install Knex**
Knex is a SQL query builder for Node.js that allows for model schema creation, migrations, connection pooling, and seeding. <br>
We want to install this globally as well as in our dependencies.
```bash
$ npm install knex -g
$ npm install knex --save
```
