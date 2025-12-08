# Banking Management System (Linux Socket)

This project implements a simple Banking Management System using C and Linux socket programming. The system uses a client-server architecture where clients can connect to the server and perform banking operations such as account creation, login, deposit, withdrawal, and balance enquiry.

## Features

- Client–server communication using Linux sockets
- User authentication (customer/admin)
- Create new bank account
- Deposit and withdraw money
- Check balance and view details
- Persistent storage of account data on server side
- Multiple clients can communicate with the server

## Technologies Used

- C programming language
- Linux/Unix socket programming (TCP/IPv4)
- File handling for storing account information
- GCC compiler

## Directory Structure

ServerAndClient/      → source code for server and client  
Modules/              → banking operation modules  
Structures/           → account/user structures and definitions  
Data/                 → stored account data and files

## How to Compile and Run

### Start the server

gcc server.c -o server  
./server <PORT>

Example:
./server 8080

### Start the client

gcc client.c -o client  
./client <SERVER_IP> <PORT>

Example:
./client 127.0.0.1 8080

After connection, the client can log in, create an account, and perform operations. All requests are sent to the server through the socket and the server responds with results.

## Operations

- Create account
- Login
- Deposit
- Withdraw
- Balance enquiry
- Logout

## Design Overview

The system uses the following flow:
- Server: socket → bind → listen → accept
- Client: socket → connect
- Server processes requests and maintains account data using files
- Communication happens over TCP using send/receive

## Future Improvements

- Add encryption for secure communication
- Use database instead of files
- Improve user interface and validation

## Conclusion

This project demonstrates the implementation of a basic banking system using Linux sockets and C. It provides hands-on understanding of client-server communication, file handling, and network programming.
