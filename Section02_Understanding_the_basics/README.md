# Module Summary

## How the Web Works

- the web is a service that runs on the internet, which is the network of computers that can communicate with each other, using the TCP/IP protocol, which is a set of rules that define how computers exchange data over the internet.

* Client => Request => Server => Response => Client

## Program Lifecycle & Event Loop

* Node.js is a JS runtime environment,`node -v` to check the version

* Node.js runs non-blocking JS code  and uses an event-driven code (“Event Loop”) for running your logic
* A Node program exists as soon as there is no more work to do, `process.exit()` can be used to exit the process explicitly.

* Node.js is single-threaded (but uses multiple threads under the hood), `process.env.UV_THREADPOOL_SIZE` to check the number of threads
  

* Note: The createServer() event never finishes by default

## Asynchronous Code

* JS code is non-blocking
* User callbacks and events => Order changes!

## Request & Responses

```javascript
const server = http.createServer((req, res) => {
  console.log(req.url, req.method, req.headers);
  // process.exit();
  res.setHeader('Content-Type', 'text/html');
  res.write('<html>');
  res.write('<head><title>My First Page</title></head>');
  res.write('<body><h1>Hello from my Node.js Server!</h1></body>');
  res.write('</html>');
  res.end();
});
```
[HTTP headers](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers)

* Parse request data in chunks (Streams & Buffers)
* Avoid “double responses”

## Node.js & Core Modules

* Node.js ships with multiple core modules (http, fs, path, ….)
* Core modules can be imported into any file to be used there
* Import via require(‘module)

## The Node Module System

* Import via require(‘./path-to-file’) for custom files or require(‘module’) for core & third-party modules
* Export via module.exports or just exports (for multiple exports)

## Useful Resources & Links

* [Official Node.js Docs](https://nodejs.org/en/docs/guides/)
* [Full Node.js Reference (for all core modules)](https://nodejs.org/dist/latest/docs/api/)
* [More about the Node.js Event Loop](https://nodejs.org/en/docs/guides/event-loop-timers-and-nexttick/)
* [Blocking and Non-Blocking Code](https://nodejs.org/en/docs/guides/dont-block-the-event-loop/)



