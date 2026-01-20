Md
Layer 2 Case Study – ARP Spoofing
What ARP Does
The Address Resolution Protocol (ARP) maps IP addresses to MAC addresses within a local network.
It assumes trust by design and does not authenticate responses.
	
How ARP Spoofing Works
An attacker send forged ARP replies to a victim, associating the attacker’s  MAC address with the IP address of a legitimate device (such as gateway).
This allows the attacker to:
Intercept traffic (Man-in-the -Middle )
Modify packets
Redirect or disrupt communication

Why Firewalls Don’t Stop This
Firewalls typically operate at Layers 3 – 7. ARP spoofing occurs entirely Layer 2 and inside the trusted network boundary.
As a result:
Encrypted traffic may still be intercepted 
Internal threat is violated without triggering perimeter defenses

Real-World Context
Shared networks such as:
Campus LANs
Office networks
Public or semi – public Wi – Fi 
are particularly vulnerable if Layer 2 protections are not enforced.
