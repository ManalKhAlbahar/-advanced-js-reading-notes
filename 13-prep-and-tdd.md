# Read13 : Message Queues
* Answer the question.
* Document the following Vocabulary Terms.
* Socket.io Chat Example.
* Rooms and Namespaces.

### *Answer the question*
- Q1: enables the server to send real-time updates asynchronously, without requiring the client to submit a request each time.

- Q2: The client will try to establish a WebSocket connection if possible, and will fall back on HTTP long polling if not.

- Q3: The event gets passed to the server through websockets. Its a tcp connection from the browser to the server. The connection is full duplex 
meaning the server can send real time data to the client and vise versa.

- Q4: Socket.io is a robust server->client->server event handler, and is really great at that.

- Q5: When mistakes happen it’s important to be honest and identify where errors have occurred.

### *Document the following Vocabulary Terms*
- Socket one endpoint of a two-way communication link between two programs running on the network.
- Web Socket WebSocket is a computer communications protocol, providing full-duplex communication channels over a single TCP connection. The 
WebSocket protocol was standardized by the IETF as RFC 6455 in 2011, and the WebSocket API in Web IDL is being standardized by the W3C. WebSocket 
is distinct from HTTP.
- Socket.io Socket.IO is a JavaScript library for realtime web applications. It enables realtime, bi-directional communication between web clients 
and servers. It has two parts: a client-side library that runs in the browser, and a server-side library for Node.js. Both components have a 
nearly identical API.
- Server The Server instance (often called io in the code examples) has a few attributes that may be of use in your application.

### *Socket.io Chat Example*
- The first goal is to set up a simple HTML webpage that serves out a form and a list of messages.
- install dependencies property with the things we need
-       npm install express@4

- creat index.js file that will set up our application.
-       const express = require('express');
       const app = express();
       const http = require('http');
       const server = http.createServer(app);
       app.get('/', (req, res) => {
       res.send('<h1>Hello world</h1>');
       });
       server.listen(3000, () => {
       console.log('listening on *:3000');
       });

- This means that:
1. Express initializes app to be a function handler that you can supply to an HTTP server (as seen in line 4).
2. define a route handler / that gets called when we hit our website home.
3.  make the http server listen on port 3000.

- Integrating Socket.IO:
Socket.IO is composed of two parts:
1. A server that integrates with (or mounts on) the Node.JS HTTP Server socket.io
2. A client library that loads on the browser side socket.io-client.

install Socket.IO
-     npm install socket.io

- ![Socket.io Chat Example](https://camo.githubusercontent.com/bdd5b0e29e317fd50a2544ea899cb871c11548a0827d2e3734a603f79106874e/687474703a2f2f692e696d6775722e636f6d2f6a565a315877692e706e67)

For more details watch this [Socket.io Chat Example](https://socket.io/get-started/chat/).

### *Rooms and Namespaces*
- This is what namespaces and rooms have in common involved a complete rewrite, so things might have changed):

- Both namespaces (io.of(‘/nsp’)) and rooms (socket.join(‘room’)) are created on the server side Multiple namespaces and multiple rooms share the 
same (WebSocket) connection The server will transmit messages over the wire only to those clients that connected to / joined a nsp / room, i.e. 
it’s not just client-side filtering The differences:

- namespaces are connected to by the client using io.connect(urlAndNsp) (the client will be added to that namespace only if it already exists on 
the server) rooms can be joined only on the server side (although creating an API on the server side to enable clients to join is straightforward) 
namespaces can be authorization protected authorization is not available with rooms, but custom authorization could be added to the 
aforementioned, easy-to-create API on the server, in case one is bent on using rooms rooms are part of a namespace (defaulting to the ‘global’ 
namespace) namespaces are always rooted in the global scope.





