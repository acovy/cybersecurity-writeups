# 🧩 TryHackMe — TCP/IP Walkthrough

## 📅 Date
2025-10-14

## 📝 Description
This walkthrough covers the **TCP/IP module** on TryHackMe.  
We explore the **TCP/IP model**, its correspondence with OSI, key protocols, and practical network examples.

> ⚡ After completing this module, you'll understand how network protocols and their layers function in practice.

---

## 🔹 Introduction
The **TCP/IP** (Transmission Control Protocol / Internet Protocol) model was developed in the **1970s by the U.S. Department of Defense (DoD)**.  
One of its main strengths is that a network can continue functioning even when parts of it are down (e.g., during an attack), thanks to adaptive routing protocols.

---

## 🔹 TCP/IP Model Layers
Unlike OSI, the TCP/IP model is often studied **from top to bottom**:

1. **Application Layer**  
   - Combines OSI layers: Application (7), Presentation (6), and Session (5)  
2. **Transport Layer** — OSI layer 4  
3. **Internet Layer** — OSI layer 3  
4. **Link Layer** — OSI layer 2  

### 🔹 TCP/IP vs OSI Comparison
| TCP/IP Layer | OSI Layers Covered | Example Protocols |
|--------------|------------------|-----------------|
| Application  | 5, 6, 7 | HTTP, HTTPS, FTP, POP3, SMTP, IMAP, Telnet, SSH |
| Transport    | 4 | TCP, UDP |
| Internet     | 3 | IP, ICMP, IPSec |
| Link         | 2 | Ethernet 802.3, WiFi 802.11 |
| Physical*    | 1 | — |

> \* Many modern textbooks include the physical layer separately, forming a **five-layer TCP/IP model**: Application → Transport → Network → Link → Physical.

---

## 🔹 Protocols Overview

### Application Layer
- Examples: HTTP, HTTPS, FTP, SMTP, SSH  
- Function: Provides services directly to applications, handles data, enables communication between end-users  

### Transport Layer
- Examples: TCP, UDP  
- Function: Ensures **end-to-end communication** between applications, handles segmentation, flow control, and error correction  

### Internet Layer
- Examples: IP, ICMP, IPSec  
- Function: Routes packets and provides logical addressing  

### Link Layer
- Examples: Ethernet, WiFi  
- Function: Transfers data within a single network segment  

---

## 🔹 Summary Table
| Layer | OSI Layers | TCP/IP Layer | Example Protocols |
|-------|------------|--------------|-----------------|
| 7 Application | 5,6,7 | Application | HTTP, FTP, SMTP |
| 4 Transport   | 4   | Transport   | TCP, UDP |
| 3 Network     | 3   | Internet    | IP, ICMP, IPSec |
| 2 Data Link   | 2   | Link        | Ethernet, WiFi |
| 1 Physical    | 1   | Physical    | — |

---

## 🔹 Questions / Tasks

**1️⃣ To which layer does HTTP belong in the TCP/IP model?**  
**Answer:** Application Layer ✅

**2️⃣ How many layers of the OSI model does the application layer in the TCP/IP model cover?**  
**Answer:** 3 ✅

---
