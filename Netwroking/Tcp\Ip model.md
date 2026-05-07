# TCP/IP Model

> The TCP/IP model has **4 layers** (unlike OSI which has 7).
> In this note uses OSI layer numbers (L1, L4, L7) to map concepts — they refer to the same ideas.

## Layers (Top → Bottom)

| TCP/IP Layer | OSI Equivalent | Role |
|---|---|---|
| Application | L5–L7 | Data formatting, compression |
| Transport | L4 | TCP / UDP |
| Network (Internet) | L3 | IP addressing, routing |
| Network Access | L1–L2 | MAC addressing, physical bits |

---

## Application Layer

- Message gets serialized: `Hello → { "msg": "Hello" }`
- Then compressed
- Then converted to binary

---

## Transport Layer

Two protocols:

### TCP — Transmission Control Protocol
- Use case: sending text messages like `"I Love You"` — every word must arrive correctly
- Packets may arrive out of order (`OIve ou`) but TCP **reassembles** them in the right order
- Guarantees: ordered, reliable, error-checked delivery
- Data unit: **Segment** → `sender port | data | receiver port`

### UDP — User Datagram Protocol
- Use case: Video Streaming, sending 10 million images (speed over reliability)
- No guarantee of delivery or order — just fire and forget
- Data unit: **Datagram** → `sender port | data | receiver port`

---

## Network Layer

- Adds IP addresses for routing across networks
- Data unit: **Packet** → `sender ip | segment / datagram | receiver ip`


---

## Data Link Layer

- Adds MAC addresses for delivery within the local network
- Data unit: **Frame** → `sender mac address | packet | receiver mac address`

---

## Physical Layer

- Converts everything to raw bits sent over cable/wifi
- `frame → bits → 0110101010101010`

---

## Data Encapsulation Flow (Sender Side)

```
App data
  → [Application]  serialize + compress → binary
  → [Transport]    add ports            → Segment / Datagram
  → [Network]      add IPs              → Packet
  → [Data Link]    add MACs             → Frame
  → [Physical]     convert              → Bits (01010101...)
```

Receiver does the reverse (decapsulation).
