# Reading Notes 301

## What is Node.js?

Node.js is an event-based, non-blocking, asynchronous I/O runtime that uses Google’s V8 JavaScript engine and libuv library. The V8 engine is the open-source JavaScript engine. It was designed with performance in mind and is responsible for compiling JavaScript directly to native machine code that your computer can execute. This means that Node.js is a program we can use to execute JavaScript on our computers. In other words, it’s a JavaScript runtime.

## Node.js Has Excellent Support for Modern JavaScript

Node has excellent support for ECMAScript 2015 (ES6) and beyond. As you’re only targeting one runtime (a specific version of the V8 engine), this means that you can write your JavaScript using the latest and most modern syntax. It also means that you don’t generally have to worry about compatibility issues — as you would if you were writing JavaScript that would run in different browsers. Node comes bundled with a package manager called npm. In addition to being the package manager for JavaScript, npm is also the world’s largest software registry. There are over 1,000,000 packages of JavaScript code available to download

## What Is Node.js Used For?

Now that we know what Node and npm are; installing (via npm) and running (via Node) various build tools designed to automate the process of developing a modern JavaScript application. These build tools come in all shapes and sizes, and you won’t get far in a modern JavaScript landscape without bumping into them. They can be used for anything from bundling your JavaScript files and dependencies into static assets, to running tests, or automatic code linting and style checking.

## Node.js Lets Us Run JavaScript on the Server

Next we come to one of the biggest use cases for Node.js, running JavaScript on the server. Node.js is single-threaded. It’s also event-driven, which means that everything that happens in Node is in reaction to an event.

https://uploads.sitepoint.com/wp-content/uploads/2012/10/1516152673node_event_loop.png
