# TLS and Encryption — What Security They Provide (and What They Do Not)

Transport Layer Security (TLS) protects internet communications, but is often **misunderstood as comprehensive security**.

---

## What TLS Actually Does

TLS provides:

- **Confidentiality** — prevents third parties from reading data  
- **Integrity** — prevents modification during transmission  
- **Authentication** — verifies server (and sometimes client) identity  

These protections apply **only while data is in transit**.

---

## What TLS Does Not Do

TLS does **not**:

- Validate user intent  
- Prevent Denial of Service (DoS) attacks  
- Stop abuse of application logic  
- Prevent malware delivery  

> TLS protects communication, **not systems**.

---

## Why Encrypted Malware Exists

Malware often uses HTTPS and encrypted channels because:

- Encrypted traffic is **trusted by default**  
- Security systems inspect it less  
- Behavior is allowed, even if content is hidden

Encryption hides **what** is sent, not **why**.

---

## TLS and DoS

TLS cannot prevent DoS:

- Handshakes consume CPU  
- Decryption is expensive  
- Attackers can overwhelm systems with legitimate-looking encrypted traffic

---

## The Dangerous Myth: “We Are Secure Because We Use HTTPS”

Blind reliance on HTTPS causes:

- Overconfidence  
- Reduced monitoring  
- Trust in encrypted channels  

> HTTPS improves privacy, but **does not prevent abuse**.

---

## Key Insight

TLS ensures **confidentiality, integrity, and authentication**, but leaves:

- User behavior  
- Application logic  
- Resource exhaustion  

…completely unprotected.  

Security must exist **before, during, and after encryption**.
