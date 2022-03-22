Rooms
A room is an arbitrary channel that sockets can join and leave. It can be used to broadcast events to a subset of clients

oining and leaving
You can call join to subscribe the socket to a given channel:

io.on("connection", socket => {
  socket.join("some room");
});
And then simply use to or in (they are the same) when broadcasting or emitting:

io.to("some room").emit("some event");
You can emit to several rooms at the same time:

io.to("room1").to("room2").to("room3").emit("some event");

Default room
Each Socket in Socket.IO is identified by a random, unguessable, unique identifier Socket#id. For your convenience, each socket automatically joins a room identified by its own id.

This makes it easy to implement private messages:

io.on("connection", socket => {
  socket.on("private message", (anotherSocketId, msg) => {
    socket.to(anotherSocketId).emit("private message", socket.id, msg);
  });
});

isconnection
Upon disconnection, sockets leave all the channels they were part of automatically, and no special teardown is needed on your part.

You can fetch the rooms the Socket was in by listening to the disconnecting event