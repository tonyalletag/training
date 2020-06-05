# Hello World - Node.js

* This tutorial is written specifically for OSX.

* Follow this tutorial to learn how to setup a basic node app on port 3000 as well as a reverse proxy through nginx.

## Install & setup node.

1. Go to https://nodejs.org/en/ ⇒ Download & Install latest latest version of Node.js (Version 8.11.2 when this tutorial was uploaded)

## Create your first Node.js application.

### Open a new terminal window and use the following commands to initialize your first app.

1. `mkdir my-node-app`

2. `cd my-node-app`

3. `npm init`

4. Click enter to use the default entries for the app name,version,description,etc.

5. Type `yes` and click enter when asked, "Is this ok?" to complete app initialization.


## Install Express into your new app's directory.

1. `npm install express --save`


## Setup your index file.

1. Create a new file in your app directory named 'index.js' (or the name of your custom entry point if not using the default)
```
var express = require('express');
var app = express();
app.get('/', function (req, res) {
  res.send('Hello World!');
});
app.listen(3000, function () {
  console.log('Your node app is running on port 3000!');
});
```
2. Save the file.

3. Go back to terminal and in your app's root directory run the following command: `node index.js`

4. Your node app should now be up and running on localhost:3000


## Redirect using nginx reverse proxy (Optional)

### Install nginx using homebrew.

1. `brew install nginx`

2. `sudo nginx` ⇒ Start nginx server

3. Check localhost:8080 ⇒ Make sure nginx server is running.

5. `sudo nginx -s stop` ⇒ Stop the server for now.


### Create and link site config folders.
1. `mkdir -p /usr/local/etc/nginx/sites-{enabled,available}`
2. `cd sites-available`
3. `touch default.conf`
4. Open default.conf with your favorite text editor and add & save the following lines of code.
```
server {
    listen 80;
    location / {
      proxy_pass http://127.0.0.1:3000;
    }

}

```

5. Go back to terminal

6. Cd to the newly created sites-enabled directory. 

   `cd /usr/local/etc/nginx/sites-enabled`

7. `ln -s ../sites-available/default.conf` => Create a symbolic link from the sites-enabled folder to the default config file you just created in the sites-available directory.



### Tell nginx to use sites-enabled.

1. Add the following line to the bottom /usr/local/etc/nginx/nginx.conf under `include servers/*;`

   `include /usr/local/etc/nginx/sites-enabled/*;`

2. `sudo nginx` ⇒ Start nginx server

3. Go to localhost with your browser to see your app running on default port 80!!!

