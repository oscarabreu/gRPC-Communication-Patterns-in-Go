# gRPC Communication Patterns in Go

This project demonstrates various gRPC communication patterns in Go, including unary, 
client streaming, server streaming, and bidirectional streaming.

## Overview

gRPC is a modern framework for building efficient and scalable remote procedure 
call (RPC) systems. It uses HTTP/2 for transport, Protocol Buffers (Protobuf) 
as the interface definition language, and provides support for multiple 
communication patterns.

In this project, we have implemented the following gRPC communication patterns:

### Unary RPC (Client to Server)

In the unary RPC pattern, the client sends a single request to the server and 
receives a single response. This pattern is useful for simple one-time requests.

`unary.go` - Client implementation.

### Client Streaming RPC (Client to Server)

Client streaming RPC allows the client to send multiple requests to the server 
and receive a single response. This pattern is suitable for scenarios where 
the client needs to send a sequence of data.

`client_stream.go` - Client implementation.

### Server Streaming RPC (Client to Server)

Server streaming RPC enables the server to send multiple responses to a single 
client request. This is useful when the server has a stream of data to send 
to the client.

`server_stream.go`- Client implementation.

### Bidirectional Streaming RPC (Client to Server and Vice V.)

Bidirectional streaming RPC allows both the client and server to send 
and receive a stream of messages concurrently. This pattern is 
well-suited for real-time communication between client and server.

`bi_stream.go` - Client implementation.

## How to Run

1. Start the gRPC server:
   Navigate to the server directory.
   Run go run main.go to start the server on port 8080.

2. Run the gRPC clients:
   Choose the client code (unary.go, client_stream.go, server_stream.go, or bi_stream.go) you want to run.
   Modify the client code to specify the desired communication pattern.
   Run the client code to interact with the gRPC server.

## Dependencies

- gRPC: The project uses the gRPC framework for communication.
- Protocol Buffers (Protobuf): Protobuf is used for defining the service and message types.

## Credit

This project was inspired by, and builds upon, code originally developed by educator AkhilSharma90. While the original project served as a foundation, this version introduces several enhancements.
