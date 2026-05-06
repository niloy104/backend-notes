
# OSI Model (Open Systems Interconnection Model)

The **OSI Model** is a conceptual networking framework that explains how data moves through a network using **7 layers**.

---

## OSI Layers (L1 → L7)

A popular mnemonic to remember the order is:

**"Please Do Not Tell Secret Password Anyone"**

| Layer | Name |
|------:|------|
| L7 | **Application Layer** |
| L6 | **Presentation Layer** |
| L5 | **Session Layer** |
| L4 | **Transport Layer** |
| L3 | **Network Layer** |
| L2 | **Data Link Layer** |
| L1 | **Physical Layer** |

---

## Practical View (What Software Engineers Use Most)

In real-world software engineering, most backend developers mainly deal with:

- **Application Layer (L7)** → HTTP, DNS, SMTP, FTP  
- **Transport Layer (L4)** → TCP/UDP, Ports  
- **Network Layer (L3)** → IP Addressing, Routing  

> Lower layers (L1–L2) are usually handled by hardware, OS, and networking devices.

---

## Visual Diagram

<img width="560" height="456" alt="OSI Model Diagram" src="https://github.com/user-attachments/assets/067f83f5-334d-40ba-aced-6284a496195c" />

📌 Reference:  
[What is OSI Model - BlueCat Networks](https://bluecatnetworks.com/glossary/what-is-the-osi-model/)

---

## Important Concepts

### Protocol Data Units (PDU)
Each layer has its own data format name:

- **Layer 3 (Network Layer)** → **Packet**
- **Layer 4 (Transport Layer)** → **Segment (TCP)** / **Datagram (UDP)**

---

## IP vs Port (Simple Explanation)

Think of it like an apartment building:

- **IP Address** = the building address (where the server is)
- **Port** = the apartment/flat number (which service inside the server)

Example:
- `192.168.1.10:80` → Web Server (HTTP)
- `192.168.1.10:5432` → PostgreSQL Database

---

## IP vs MAC Address

- **IP Address** = logical / virtual address (changes depending on network)
- **MAC Address** = physical hardware address (unique to the network card)

---
