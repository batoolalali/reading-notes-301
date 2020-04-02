### How Heroku Works
Heroku lets you deploy, run and manage applications written in Ruby, Node.js, Java, Python, Clojure, Scala, Go and PHP.

Heroku lets you deploy, run and manage applications written in Ruby, Node.js, Java, Python, Clojure, Scala, Go and PHP.

- in Node.js a package.json

#### Terminology:
- Preliminary: Applications consist of your source code and a description of any dependencies.
- Procfiles list process types - named commands that you may want executed.
- Deploying applications involves sending the application to Heroku using either Git, GitHub, or via an API.
- slug : a bundle of your source, fetched dependencies, the language runtime, and compiled/generated output of the build system - ready for execution.
- Dynos are isolated, virtualized Unix containers, that provide the environment required to run an application.


**Deploying applications**
- deploying code is just the familiar git push
`$ git push heroku master`

**Building applications**
When the Heroku platform receives the application source, it initiates a build of the source application. 

- First step after Heroku installation is to log in to the system from your computer:
`$ heroku login`

- npm install
`$ npm install`

- To start your server locally run:
`$ node server.js`