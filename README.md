# TCP/IP Network Simulator exe

---

## Description

The Mini TCP/IP Network Simulator is a graph-based interactive application developed in Python that simulates packet transmission in a computer network. The simulator allows users to create network topologies dynamically, define link conditions, and visualize routing, congestion, and acknowledgment mechanisms in a mesh network.

The system focuses on simplified TCP/IP concepts, particularly routing decisions under link constraints such as good, congested and faulty connections.

This project allows users to **create a custom network topology**, simulate **multi-source packet transmission**, and observe **real-time packet flow with queuing and link contention**

---

## Features

- **Dynamic Network Creation**
  - Add nodes interactively
  - Connect nodes with different link types

- **Link Types**
  - **Green (Good)** → Fast transmission
  - **Yellow (Congested)** → Slower transmission (2× delay)
  - **Red (Bad)** → Completely blocked (not used for routing)

- **Packet Transmission**
  - Send multiple packets between nodes
  - Round-robin distribution across multiple paths
  - Path selection avoids bad links

- **Routing Logic**
  - Dijkstra-like weighted path selection
  - Green links preferred over yellow
  - Automatic multi-path routing

- **TCP-like Behavior**
  - Sequence-numbered packets
  - Acknowledgment (ACK) packets
  - Pipelined transmission

- **Visualization**
  - Real-time packet movement animation
  - ACK animation (reverse path)
  - Queueing on busy links

- **Full-Duplex Communication**
  - Simultaneous DATA and ACK transmission allowed
  - Models modern network behavior

---

## Tech Stack

- **Language:** Python 3
- **GUI:** Tkinter
- **Core Concepts:**
  - Computer Networks
  - TCP/IP Protocol
  - Graph Algorithms
  - Event Simulation

---

## How to Run

- Download the TCP-IP Simulator .exe file and open it

---

## Usage

1. Add Nodes
- Click Add Node and click on canvas
2. Create Links
- Select:
  - Good Link (Green)
  - Congested Link (Yellow)
  - Bad Link (Red)
- Click two nodes to connect
3. Send Packets
- Select Send Packets
- Choose source and destination
- Enter number of packets
4. Start Simulation
- Click Start Simulation

---

## Simulation Behavior

- Packets are routed using shortest weighted paths
- Red links are never used
- Yellow links introduce delay
- Multiple packets:
  - Use different paths (load balancing)
  - Wait if link is busy
- ACK packets:
  - Travel back to sender
  - Simulate TCP acknowledgment

---

## Author

Prathamesh Gawas

---
