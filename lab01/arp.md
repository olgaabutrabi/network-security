# ARP Spoofing & Dynamic ARP Inspection

**Tools:** Kathará, Open vSwitch, tcpdump, Wireshark

## Objective
Demonstrate an ARP spoofing attack and prevent forged ARP messages using switch filtering rules.

## Implementation
- Set up a simulated network in Kathará and captured traffic with `tcpdump`.
- Ran an ARP spoofing script on Mallory to redirect traffic between Alice and Bob.
- Verified the attack by checking Alice's ARP cache: Bob's IP (`10.0.0.12`) was mapped to Mallory's MAC (`00:00:00:00:00:14`).
- Captured the redirected ICMP traffic on Mallory.
- Added Open vSwitch rules to validate ARP sender IP/MAC bindings and drop invalid ARP packets.

## Result
After enabling the filtering rules, Alice's ARP cache showed Bob's correct MAC address again (`00:00:00:00:00:12`), and the spoofing attack was blocked.