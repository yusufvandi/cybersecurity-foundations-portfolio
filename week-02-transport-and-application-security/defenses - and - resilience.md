# Defenses and Resilience — Designing for Failure

Good defensive design begins with the expectation that **assumptions will fail**.  

A resilient system assumes:

- Attacks will appear legitimate  
- Defensive controls may fail  
- Trust relationships can be exploited  

Defense is **not about preventing all attacks**, but **limiting damage when failure occurs**.

---

## Rate Limiting — Controlling Trust

Rate limiting assumes that:

- Trust is exploitable  
- Unlimited trust is dangerous  

It reduces abuse and prevents single sources from overwhelming the system.

---

## Timeouts — Expiring Trust

Timeouts prevent:

- Hanging sessions  
- Long-term resource allocation without proof of value  

> *“Prove value quickly or lose access.”*

---

## Logging and Detection — Visibility into Failure

Logging acknowledges that breaches occur. Detection focuses on:

- Patterns  
- Anomalies  
- Behavior over time  

Failures become **detectable and actionable**, rather than silent.

---

## Defense-in-Depth at Higher Layers

No single control is sufficient.  
Multiple weaker controls can **outperform one strong control**.  

Layered design ensures that failure of one mechanism does **not** lead to total compromise.

---

## Key Insight

A good defense is **not built for perfection**.  
It is built for **resilience** — systems that **expect failure** and **survive it intelligently**.
