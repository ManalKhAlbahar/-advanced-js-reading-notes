# Read08
* Answer the question.
* Event Driven Programming.
* Node docs: events.
* wiki - RBAC.

### *Answer the question*
- Q1: Access control is important because it is a valuable security technique that can be used to regulate who or what can view or use any given 
resource. In an I.T security setting this could translate to who can access and edit a particular file, what kinds of equipment can be used or who 
can access certain devices. 
- Q2: 



### *Event Driven Programming*
- Event-Driven Programming is a logical pattern that we can choose to confine our programming within to avoid issues of complexity and collision.

- Event-Driven Programming makes use of the following concepts:
1. An Event Handler is a callback function that will be called when an event is triggered.
2. A Main Loop listens for event triggers and calls the associated event handler for that event.

- EventEmitter:
Node.js natively provides us with a useful module called EventEmitter that allows us to get started incorporating Event-Driven Programming in our 
project right away.

- access the EventEmitter class through the events module. 
     const EventEmitter = require('events').EventEmitter;
     const myEventEmitter = new EventEmitter;

- Removing Listeners:
There will likely come a time when you want to remove an event listener from an event. This could be for performance reasons (the event is no 
longer needed) or to avoid memory leaks (if an event listener references an object that is no longer needed, it won’t be able to be 
garbage-collected. This can lead to a build up of unnecessary objects).

To remove event listeners in EventEmitter we can use the removeListener or removeAllListeners method. 

- Object Oriented Programming + Event-Driven Programming:
the combination of the Object Oriented and Event-driven programming paradigms. These two make for a very valuable combination in a wide variety of 
situations.

The Object Oriented approach promotes the idea that all behavior of an individual unit (or object) be handled from code within that unit. Using 
this approach, applications are built with many different units that all speak to and interact with each other.

For more details watch this [Event Driven Programming](https://www.digitalocean.com/community/tutorials/nodejs-event-driven-programming).

### *Node docs: events*
- Much of the Node.js core API is built around an idiomatic asynchronous event-driven architecture in which certain kinds of objects (called 
"emitters") emit named events that cause Function objects ("listeners") to be called.
T
- Passing arguments and this to listeners : The eventEmitter.emit() method allows an arbitrary set of arguments to be passed to the listener 
functions. Keep in mind that when an ordinary listener function is called, the standard this keyword is intentionally set to reference the 
EventEmitter instance to which the listener is attached.

- Asynchronous vs. synchronous : The EventEmitter calls all listeners synchronously in the order in which they were registered. This ensures the 
proper sequencing of events and helps avoid race conditions and logic errors. When appropriate, listener functions can switch to an asynchronous 
mode of operation using the setImmediate() or process.nextTick() methods .

- Handling events only once : When a listener is registered using the eventEmitter.on() method, that listener is invoked every time the named 
event is emitted.
Using the eventEmitter.once() method, it is possible to register a listener that is called at most once for a particular event. Once the event is  
emitted, the listener is unregistered and then called.

- Error events : When an error occurs within an EventEmitter instance, the typical action is for an 'error' event to be emitted. These are treated 
as special cases within Node.js.
If an EventEmitter does not have at least one listener registered for the 'error' event, and an 'error' event is emitted, the error is thrown, a 
stack trace is printed, and the Node.js process exits.

For more details see [Node docs: events](https://nodejs.org/api/events.html).

