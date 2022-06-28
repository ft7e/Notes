# Message Queues

## Chat example

Sockets have traditionally been the solution around which most real-time chat systems are architected, providing a bi-directional communication channel between a client and a server The server can push messages to clients

Whenever you write a chat message, the idea is that the server will get it and push it to all other connected clients

## Rooms

A room is an arbitrary channel that sockets can join and leave. It can be used to broadcast events to a subset of clients:

Joining and leaving You can call join to subscribe the socket to a given channel
