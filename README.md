# Date and Time Client-Server-Project
This project implements a simple server-client system where the client requests the current date and time from the server, and the server responds with the information.

## Features
- **Server**: Listens for incoming client connections and sends the current date and time to each client that connects.
- **Client**: Connects to the server and prints the received date and time to the console.

## How It Works
### Server
- The server runs on a specified port, waits for a client connection, and sends the current date and time when a client connects.
- Continues running, ready to accept new clients.

### Client
- The client connects to the server using the server's IP address and port number.
- Receives the current date and time from the server and prints it.

## Files
- `server.c`: Contains the server code that listens for client connections and sends the date and time.
- `client.c`: Contains the client code that connects to the server and receives the date and time.
- `Practical.h`: A header file with utility functions for handling errors.

## How to Compile and Run
### Prerequisites
- A Linux system with GCC installed or any system that supports `socket.h` and TCP/IP networking.
- Basic knowledge of C programming.

### Compilation
To compile the server and client, use the following commands:
1. **Compile the server**:
   ```bash
   gcc -o server server.c Practical.c
2. **Compile the client**:
   ```bash
   gcc -o client client.c Practical.c

### Running the Application
1. **Run the server**:
   On the server machine or terminal, run the server program, specifying the port on which it should listen for connections:
   ```bash
   ./server 8080
3. **Run the client**:
   On the client machine or terminal, connect to the server using its IP address and the same port:
   ```bash
   ./client <Server IP> 8080

### Example Output
**Server**
Server started and listening on port 8080...
Client connected. Sending date and time: Wed Oct 16 14:30:00 2024

**Client**
Received from server: Wed Oct 16 14:30:00 2024
