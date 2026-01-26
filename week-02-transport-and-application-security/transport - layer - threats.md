# Transport Layer Threats — TCP and Trust Abuse

The Transport Layer is responsible for end-to-end communication between applications.
Its core responsibilities include:

- Ordering data
- Flow control
- Congestion control
- Maintaining stateful connections

This **statefulness enables reliability**, but it also introduces **trust assumptions** that can be exploited.

---

## TCP and the Three-Way Handshake

TCP establishes connections using a three-way handshake:

1. **SYN** — The client requests a connection  
2. **SYN-ACK** — The server acknowledges the request and allocates resources  
3. **ACK** — The client confirms, and data transfer begins  

TCP assumes that:

- The client intends to complete the handshake  
- The client is reachable  
- The connection request is legitimate  

These assumptions are **intentional design choices**, not accidental flaws.

---

## Why TCP Was Designed This Way

The Internet was designed for:

- Openness  
- Scalability  
- Performance  

TCP prioritizes:

- Fast connection establishment  
- Compatibility across billions of devices  
- Minimal authentication at lower layers  

No verification occurs during the handshake; authentication is deferred to higher layers.  
This design enables global connectivity — but creates exploitable trust.

---

## SYN Flood Attacks

In a SYN flood attack, an attacker sends a large number of SYN packets to a server.

For each SYN request, the server:

- Allocates memory  
- Reserves a connection slot  
- Waits for the final ACK  

The attacker **never completes the handshake**.  
This traffic is **valid TCP traffic**, and the server behaves **exactly as designed**.

---

## Denial of Service Through Resource Exhaustion

SYN floods exploit **finite system resources**:

- CPU  
- Memory  
- Connection tables  
- Time  

When these resources are exhausted:

- Legitimate users are denied service  
- Higher-layer applications fail  

This makes SYN floods a classic **Denial of Service (DoS)** attack.

---

## Why Valid Traffic Can Be Malicious

Many security systems assume:

- Malicious traffic is malformed  
- Attacks violate protocol rules  

SYN floods demonstrate the opposite:

- Traffic is protocol-compliant  
- Abuse occurs within normal behavior  

TCP allocates resources **before verifying identity**, creating an **asymmetric cost**:

- Cheap for the attacker  
- Expensive for the server  

Attackers **cooperate dishonestly with the system**.

---

## Key Insight

SYN flood attacks succeed **not because TCP is weak**, but because
**performance-driven trust is exploitable**.  

This pattern recurs at higher layers of the network stack.
