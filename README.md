Files manager
=

This project is a summary of this back-end trimester: authentication, NodeJS, MongoDB, Redis, pagination and background processing.

The objective is to build a simple platform to upload and view files:

* User authentication via a token

* List all files

* Upload a new file

* Change permission of a file

* View a file

* Generate thumbnails for images

You will be guided step by step for building it, but you have some freedoms of implementation, split in more files etc… (utils folder will be your friend)

Of course, this kind of service already exists in the real life - it’s a learning purpose to assemble each piece and build a full product.

Enjoy!

<h2>Resources</h2>

* Node JS getting started

* Process API doc

* Express getting started

* Mocha documentation

* Nodemon documentation

* MongoDB 

* Bull

* Image thumbnail 

* Mime-Types

* Redis 

<h2>Requirements</h2>

* Allowed editors: vi, vim, emacs, Visual Studio Code

* All your files will be interpreted/compiled on Ubuntu 18.04 LTS using node (version 12.x.x)

* All your files should end with a new line

* A README.md file, at the root of the folder of the project, is mandatory

* Your code should use the js extension

* Your code will be verified against lint using ESLint


Provided files
---
<h2>package.json</h2>

Click to show/hide file contents

<h2>.eslintrc.js</h2>

Click to show/hide file contents

<h2>babel.config.js</h2>

Click to show/hide file contents

and…

Don’t forget to run $ npm install when you have the package.jso

           bob@dylan:~$ cat main.js
          import redisClient from './utils/redis';

        (async () => {
          console.log(redisClient.isAlive());
          console.log(await redisClient.get('myKey'));
          await redisClient.set('myKey', 12, 5);
          console.log(await redisClient.get('myKey'));

         setTimeout(async () => {
         console.log(await redisClient.get('myKey'));
       }, 1000*10)
    })();

      bob@dylan:~$ npm run dev main.js
        true
        null
        12
        null