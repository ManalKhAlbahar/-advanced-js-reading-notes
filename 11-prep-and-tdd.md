# Read11
* Answer the question.
* Event Driven Programming.
* Node docs: events.

### *Answer the question*
- Q1: Access control is important because it is a valuable security technique that can be used to regulate who or what can view or use any given 
resource. In an I.T security setting this could translate to who can access and edit a particular file, what kinds of equipment can be used or who 
can access certain devices. 

- Q2: roles are required for an extreme programming project to work and the persons who take these roles take the corresponding responsibilities 
and are accountable for their contribution to these roles. It is advised to allocate the right people for the roles rather than trying to change 
the people to fit into those roles.

- Q3: Role-based access control (RBAC), also known as role-based security, is an access control method that assigns permissions to end-users based 
on their role within your organization. RBAC provides fine-grained control, offering a simple, manageable approach to access management that is 
less error-prone than individually assigning permissions. 

- Q4: 1. DAC is the way to go to let people manage the content they own. It might sound obvious, but for instance DAC is very good to let users an 
online social network choose who accesses their data. It allows people to revoke or forward privileges easily and immediately. Reactive access 
control, Seeing further and Laissez-faire file sharing provide nice examples of research on DAC with users.

2. RBAC is a form of access control which as you said is suitable to separate responsibilities in a system where multiple roles are fulfilled. 
This is obviously true in corporations (often along with compartmentalization e.g. Brewer and Nash or MCS) but can also be used on a single user 
operating system to implement the principle of least privilege. RBAC is designed for separation of duties by letting users select the roles they 
need for a specific task. The key question is whether you use roles to represent tasks performed on your system and assign roles in a central 
authority (in which case RBAC is a form of MAC); or if you use roles to let users control permissions on their own objects (leading to multiple 
roles per object and absolutely no semantics in roles, even though it's theoretically possible).

3. MAC in itself is vague, there are many many ways to implement it for many systems. In practice, you'll often use a combination of different 
paradigms. For instance, a UNIX system mostly uses DAC but the root account bypasses DAC privileges. In a corporation, beyond separating your 
different departments and teams with MAC/RBAC you may allow some DAC for coworkers to share information on your corporate file system.



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

