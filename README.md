
# gRPC Client TP

This repository contains the **gRPC client** implementation for the Calculator TP in the "Architecture des composants d’entreprise" module.  
The client can interact with the server using all four gRPC communication models:

1. **Unary** – single request → single response.  
2. **Server Streaming** – single request → multiple responses.  
3. **Client Streaming** – multiple requests → single response.  
4. **Bidirectional Streaming** – multiple requests ↔ multiple responses.

---

## Features

- Calls `CalculatorService` on a gRPC server.
- Implements clients for:
  - `UnaryModelClient`
  - `ServerStreamingClient`
  - `ClientStreamingClient`
  - `BidirectionalModelClient`
- Uses **Java 17** and **Maven**.
- Requires the gRPC server running on `localhost:9999`.

---

## Project Structure

```
grpc-client-tp/
├─ src/
│ ├─ main/
│ │ ├─ java/
│ │ │ └─ ma/formations/grpc/
│ │ │ ├─ UnaryModelClient.java
│ │ │ ├─ ServerStreamingClient.java
│ │ │ ├─ ClientStreamingClient.java
│ │ │ └─ BidirectionalModelClient.java
│ │ └─ resources/
│ │ └─ calculator.proto
├─ pom.xml
└─ README.md
```



---

## How to Run

1. Compile and generate gRPC stubs:

```bash
mvn clean install

```

2. Run the desired client:
```bash
java ma.formations.grpc.UnaryModelClient
```
- Replace UnaryModelClient with any of the other client classes to test streaming modes.

# Notes
- Make sure the gRPC server is running on localhost:9999 before executing clients.

- Each client demonstrates a different gRPC communication model.


