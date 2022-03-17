# Read12 : Socket.io
* Answer the question.
* Socket.io.
* client-api. 


### *Answer the question*
- Q1: TDM-based networks must transform into packet-based networks to meet the demands of pervasive data-centric applications and 
services. Packet

- Q2: No connection needs to be established between the source and destination before you transmit data. UDP does not have a mechanism 
to make sure that the payload is not corrupted. As a result, the application must take care of data integrity all by itself.
 
- Q3: Multiple connections on the same server can share the same server-side IP/Port pair as long as they are associated with different 
client-side IP/Port pairs, and the server would be able to handle as many clients as available system resources allow it to. 

- Q4: A connected socket is assigned to a new (dedicated) port, so it means that the number of concurrent connections is limited by the 
number of ports, unless multiple sockets can share the same port.

- Q5: If you want to have a “peer-to-peer” type system, then you just have each client run both a client and a server socket - the 
server socket for accepting connections from other clients and the client socket for establishing connections to others.

### *Socket.io*
- Socket.IO is a JavaScript library for realtime web applications. It enables realtime, bi-directional communication between web 
clients and servers. It has two parts: a client-side library that runs in the browser, and a server-side library for Node.js.Both 
components have a nearly identical API. Like Node.js, it is event-driven.

- Socket.IO primarily uses the WebSocket protocol with polling as a fallback option, while providing the same interface. Although it 
can be used as simply a wrapper for WebSocket, it provides many more features, including broadcasting to multiple sockets, storing data 
associated with each client, and asynchronous I/O.

- WebSocket is a computer communications protocol, providing full-duplex communication channels over a single TCP connection.The 
current specification is known as the HTML Living Standard. It is maintained by the Web Hypertext Application Technology Working Group 
(WHATWG), a consortium of the major browser vendors (Apple, Google, Mozilla, and Microsoft).

- WebSocket is distinct from HTTP. Both protocols are located at layer 7 in the OSI model and depend on TCP at layer 4. Although they 
are different, RFC 6455 states that WebSocket "is designed to work over HTTP ports 443 and 80 as well as to support HTTP proxies and 
intermediaries", thus making it compatible with HTTP. To achieve compatibility, the WebSocket handshake uses the HTTP Upgrade header
to change from the HTTP protocol to the WebSocket protocol.

- What Socket.IO is Socket.IO is a library that enables low-latency, bidirectional and event-based communication between a client and a server.

- Server API

 ![Server API](https://socket.io/images/server-class-diagram-server.png)

- Server Installation : 
     npm install socket.io

- Additional packages :
By default, Socket.IO use the WebSocket server provided by the ws package.

There are 2 optional packages that can be installed alongside this package. These packages are binary add-ons which improve certain 
operations. Prebuilt binaries are available for the most popular platforms so you don't necessarily need to have a C++ compiler 
installed on your machine.

1. bufferutil: Allows to efficiently perform operations such as masking and unmasking the data payload of the WebSocket frames.
2. utf-8-validate: Allows to efficiently check if a message contains valid UTF-8 as required by the spec.
To install those packages:
         npm install --save-optional bufferutil utf-8-validate

### *client-api*  

- IO :The io method is bound to the global scope in the standalone build:
      <script src="/socket.io/socket.io.js"></script>
     <script>
     const socket = io();
      </script>

- io.protocol <number>
 The protocol revision number (currently: 5).

The protocol defines the format of the packets exchanged between the client and the server. Both the client and the server must use the 
same revision in order to understand each other.     

- Manager:
 
![Manager](https://socket.io/images/client-class-diagram-manager.png)        

* The Manager manages the Engine.IO client instance, which is the low-level engine that establishes the connection to the server (by 
using transports like WebSocket or HTTP long-polling).

* The Manager handles the reconnection logic.

* A single Manager can be used by several Sockets. You can find more information about this multiplexing feature here.

For more details see [client-api](https://socket.io/docs/v4/client-api).
