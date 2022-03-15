Much of the Node.js core API is built around an idiomatic asynchronous event-driven architecture in which certain kinds of objects (called "emitters") emit named events that cause Function objects ("listeners") to be called.

Event-Driven Programming is a logical pattern that we can choose to confine our programming within to avoid issues of complexity and collision. 

Event-Driven Programming makes use of the following concepts:

An Event Handler is a callback function that will be called when an event is triggered.
A Main Loop listens for event triggers and calls the associated event handler for that event.

ll objects that emit events are instances of the EventEmitter class. These objects expose an eventEmitter.on() function that allows one or more functions to be attached to named events emitted by the object. Typically, event names are camel-cased strings but any valid JavaScript property key can be used.

When the EventEmitter object emits an event, all of the functions attached to that specific event are called synchronously. Any values returned by the called listeners are ignored and discarded.

