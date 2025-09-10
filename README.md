# Chat-UDP-1.0 2023/02

![Badge](https://img.shields.io/badge/Educational-blue?style=for-the-badge&logo=academia) \
![PUCRS](https://img.shields.io/badge/Made%20at-PUCRS-blue?style=flat-square&logo=bookstack&logoColor=white)


> This project was developed as part of the Computer Networks Laboratory course during the undergraduate program at PUC-RS (Pontifícia Universidade Católica do Rio Grande do Sul). It is intended for educational purposes and may not be production-grade.

## Introduction: UDP Chat System — Server/Client over Datagram Sockets

This project implements a **chat application over UDP** using two core C programs: a *server* that manages client connections and messaging logic, and a *client* that forks into two processes — one for sending, one for receiving. Users can join the chat (`/lin <name>`), send public (`/msg <text>`) and private messages (`/mpv <user> <text>`), and even transmit files (`/arq <path>`), which the server broadcasts with metadata (filename, type, size) before relaying the file itself.

### Key Features:

* **UDP-based messaging**: no TCP overhead, fast datagram communication.
* **Multiprocess client design**: one process sends, another listens.
* **File transfer support**: small files can be shared with all online users.
* **Command-based interaction**: clean, extensible CLI interface.

### What is UDP?

* **UDP (User Datagram Protocol)** is a lightweight, connectionless transport protocol.
* It **does not guarantee delivery, ordering, or reliability** — making it faster but less safe than TCP.
* Ideal for **broadcast, real-time apps, and lightweight communications**, like chat, streaming, or DNS queries.

