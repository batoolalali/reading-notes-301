# Node.js 

### What Is Node and When Should I Use It?

- Node.js is a JavaScript runtime built on Chrome’s V8 JavaScript engine.
- Node.js is an event-based, non-blocking, asynchronous I/O runtime that uses Google’s V8 JavaScript engine and libuv library.

###### What Is V8 Engine?
is the open-source JavaScript engine that runs in Google Chrome and other Chromium-based web browsers.

### How Do I Install Node.js?

1. When working with Node.js, you might encounter situations where you need to install multiple versions of the runtime. (nvm)
`$ curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.35.2/install.sh | bash`
2. to check that you installed the node 
` $ node -v`
3. create a new file hello.js and code ...
4. run the hello.js
`$ node hello.js`

### Introducing npm, the JavaScript Package Manager
Node comes bundled with a package manager called npm. To check which version you have installed on your system, type `$ npm -v`.

###### Installing a Package Globally

1. `$ npm install -g jshint`
2. lint the index.js file by `$ jshint index.js`


###### Installing a Package Locally

1. `$npm init -y`
This will create and auto-populate a package.json file in the same folder.
2. install the lodash package and save it as a project dependency
`$ npm install lodash --save`

### What Is Node.js Used For?
- automate the process of developing a modern JavaScript application.
- Node.js Lets Us Run JavaScript on the Server

### What Kind of Apps Is Node.js Suited To?
CodeShare

### What Are the Advantages of Node.js?

- Aside from speed and scalability.
- speaks JSON. JSON is probably the most important data exchange format on the Web.
- JavaScript is ubiquitous: most of us are familiar with JavaScript, or have used it at some point. This means that transitioning to Node development is potentially easier than to other server-side languages.