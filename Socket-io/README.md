# Sockets

As per the conventional definition, WebSocket is a duplex protocol used mainly in the client-server communication channel. It’s bidirectional in nature which means communication happens to and fro between client-server.

## What does the event handler io.on() do

What Socket.IO
Socket.IO is a library that enables real-time, bidirectional and event-based communication between the browser and the server. It consists of:

a Node.js server: Source | API a Javascript client library for the browser (which can be also run from Node.js): Source | API

## Socket.io vs Web Sockets

WebSocket
It is the protocol that is established over the TCP connection

It provides full-duplex communication on TCP connections.

Proxy and load balancer is not supported in WebSocket.

It doesn’t support broadcasting.

It doesn’t have a fallback option.

## How to use

`const server = require('http').createServer(); const io = require('socket.io')(server); io.on('connection', client => { client.on('event', data => { /* … */ }); client.on('disconnect', () => { /* … */ }); }); server.listen(3000);`
