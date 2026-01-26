# Week 2 — Transport & Application Layers: Trust, Encryption, and Availability

## Purpose
This week builds on **Week 1 (Layer 2 trust failures)** and examines how the same trust assumptions **cascade upward** into the Transport and Application layers.

The goal is not tool usage, but **thinking clearly about how modern attacks succeed without breaking protocols**.

---

## Why Transport & Application Layers Matter
Most real-world attacks today do **not** rely on malformed packets or broken encryption.
Instead, they operate **inside correctly functioning systems** by exploiting:

- Trusted connections
- Encrypted channels
- Assumed “normal” behavior

Understanding this layer is critical because it is where **availability, trust, and business logic intersect**.

---

## Key Insights from This Week

### 1. Availability *is* a Security Property
Security is not only about secrecy or correctness.
A system that is:
- Slow
- Exhausted
- Hanging
- Unresponsive  

…is effectively **compromised**, even if encryption and authentication remain intact.

---

### 2. Encryption ≠ Safety
Transport Layer Security (TLS) provides:
- Confidentiality
- Integrity
- Authentication (of endpoints)

But it **does not**:
- Validate user intent
- Prevent abuse of application logic
- Stop denial-of-service
- Prevent malware activity

Encrypted traffic is often **trusted more than unencrypted traffic**, which attackers actively exploit.

> **Key insight:** TLS protects communication — not consequences.

---

### 3. Protocols Behave as Designed — Attackers Exploit That
Protocols like HTTPS, TCP, and authenticated sessions are **working correctly** during many attacks.

Attackers succeed because they:
- Blend into legitimate behavior
- Reuse trusted channels
- Exploit assumptions that persist too long

They don’t fight systems — **they cooperate dishonestly with them**.

---

## Defensive Thinking Introduced

This week emphasized **resilience over perfection**.

Good defenses assume:
- Attacks will look legitimate
- Controls will fail
- Trust will be abused

Practical mechanisms explored:
- **Rate limiting** — minimizing how much trust any source receives
- **Timeouts** — forcing early proof of value
- **Logging & detection** — accepting breaches and prioritizing visibility

> A strong defense is not one that never fails —  
> but one that **fails safely and recovers quickly**.

---

## How This Connects to Week 1
- **Week 1** showed *where* trust breaks (Layer 2).  
- **Week 2** explains *why* those same failures succeed at higher layers.

The pattern is consistent:
> Trust assumptions made low in the stack silently power failures higher up.

---

## What Comes Next (Week 3)
With trust failures understood conceptually, the next step is to examine:
- How these failures **cascade into full compromise**
- Where tooling helps — and where it doesn’t
- Why detection and response matter more than perimeter defenses

Tools return in Week 3 — **but only after the thinking is solid**.

---

## Summary
Security at higher layers is less about blocking traffic and more about:
- Reducing implicit trust
- Expiring assumptions quickly
- Designing systems that expect misuse

**Defense is not only protection — it’s intelligent survival.**
