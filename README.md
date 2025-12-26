# Reliable Transport Protocol (RTP) Project

**Author:** Vania Munjar  
**GTID:** 903871348  
**Semester:** Spring 2025

---

## Project Overview

This project implements a **Reliable Transport Protocol (RTP)** on top of a simulated network. The goal is to explore the transport layer of the network stack and implement reliability features for message delivery.

Key features include:

- Segmentation of messages into packets and reassembly at the receiver.
- Checksum calculation for error detection.
- Stop-and-Wait protocol with:
  - Positive ACK (Acknowledgements)
  - Negative NACK (Retransmissions)
- Multi-threaded client-server communication.
- Encryption and decryption of messages between client and server.

---

## File Structure

File Structure
project_5/
src/
- client.c – RTP client implementation
- network.c – Simulated network functions
- network.h
- queue.c – Thread-safe message queue
- queue.h
- rtp.c – RTP protocol implementation
- rtp.h
- rtp-server.py – Python server for testing (optional)
Makefile
Project 5.pdf – Project description/documentation

---
Running the Project
To run the project, first start the server by running ./server <port>. Then start the client and connect to the server using ./client <host> <port>. You can send messages from the client, and the server will decrypt the messages and send them back. The client will print the decrypted message.

Key Concepts Implemented:
Packetization: Messages are split into fixed-size packets.
Checksum: Detects corrupted packets using a custom algorithm.
Stop-and-Wait Protocol: Ensures reliable delivery with ACK/NACK.
Threading: Separate threads handle sending and receiving messages.
Queueing: Thread-safe message queues for send/receive operations.

---
## Building the Project

1. Make sure you have **gcc** installed.
2. Navigate to the `src/` folder.
3. Compile using the provided `Makefile`:

