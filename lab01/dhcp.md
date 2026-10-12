# Rogue DHCP & DHCP Snooping

## Objective
Understand how a rogue DHCP server can assign malicious network settings to clients and how DHCP Snooping prevents unauthorized DHCP server responses.

## Tools & Technologies
Kathará, Open vSwitch, tcpdump/Wireshark, DHCP

## Implementation & Analysis (Lab Tasks)
- Capture the DHCP address assignment process (Discover, Offer, Request, Acknowledgment).
- Simulate a rogue DHCP server advertising the attacker's IP address as the default gateway and DNS server.
- Investigate DHCP starvation as a way to exhaust the legitimate server's address pool.
- Configure DHCP Snooping to allow DHCP server responses only on trusted switch ports.
- Verify that clients receive network settings from the legitimate DHCP server after protection is enabled.

## Expected Security Outcome
DHCP Snooping blocks DHCP server responses arriving on untrusted ports, reducing the risk of clients accepting malicious gateway and DNS settings.

