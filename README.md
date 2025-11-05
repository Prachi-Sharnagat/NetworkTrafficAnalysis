# 📡 Network Traffic Analysis: UDP vs. TCP ⚖️

### A Computer Networks Project using Wireshark to capture and analyze the real-world differences between **UDP/RTP (for VoIP)** and **TCP (for file downloads)**.

## Demo Youtube Link : 
### Part1 : https://youtu.be/wqf7Qwoz6xM
### Part2 : https://youtu.be/9XGlX9BFgQE
## 🎯 Project Objective

The aim of this experiment was to use the **Wireshark network protocol analyzer** to capture and compare the traffic characteristics of:

- 🗣️ **A real-time Voice over IP (VoIP) call**, which prioritizes *speed* and *low latency*.
- 💾 **A large File Download**, which prioritizes *reliability* and *data integrity*.

This experiment provides **practical, empirical evidence** of the fundamental differences between **UDP/RTP** and **TCP** protocols.

---

## 🧰 Tools Used

| Tool | Purpose |
|------|----------|
| 🕵️ **Wireshark (v4.x)** | Network traffic capturing and analysis |
| 💬 **Discord (Desktop Client)** | Source of real-time VoIP traffic |
| 🌐 **Google Chrome** | Used for downloading an Ubuntu ISO file to generate TCP traffic |

---

## 📊 Key Findings & Analysis

### 🅰️ VoIP (RTP/UDP) Traffic

- **Protocol:** UDP (with RTP)  
- **Traffic Type:** Continuous stream of small, consistently sized packets  
- **Connection Type:** *Connectionless*  
- **Observation:** Minor packet loss (~0.16%) detected, but no noticeable lag during the call.  
- **Interpretation:** UDP prioritizes *speed* and *low latency*, tolerating small losses for real-time performance.  

---

### 🅱️ File Download (TCP) Traffic

- **Protocol:** TCP  
- **Traffic Type:** Structured packets with varying sizes, including retransmissions  
- **Connection Type:** *Connection-oriented* (established via 3-Way Handshake: `[SYN] → [SYN, ACK] → [ACK]`)  
- **Observation:** All packets were acknowledged; lost packets were retransmitted.  
- **Interpretation:** TCP ensures *reliability* and *data integrity*, making it ideal for downloads and web traffic.  

---

## 🧩 Conclusion

The experiment successfully demonstrated the **speed vs. reliability trade-off**:

| Protocol | Used For | Priority | Trade-Off |
|-----------|-----------|-----------|------------|
| **UDP/RTP** | Real-time apps (VoIP, video streaming, gaming) | Speed, low latency | Possible packet loss |
| **TCP** | File transfer, email, web browsing | Reliability, accuracy | Higher latency |

> **Summary:**  
> UDP/RTP favors real-time speed, while TCP guarantees data integrity.

---

## 👩‍💻 **Contributors**
1. Rashi Sukhwani
2. Mansi Gupta	
3. Prachi Sharnagat

