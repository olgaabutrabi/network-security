# SSH – Handshake and Host Authentication

## Objective
Examine how SSH negotiates cryptographic algorithms, establishes session keys, and authenticates a server.

## Tools & Technologies
OpenSSH, Wireshark, SSH.

## Implementation & Analysis
- Connected to a university SSH server and checked its host-key fingerprint against a trusted reference.
- Captured the connection setup and examined protocol identification, key-exchange initiation, Diffie–Hellman messages, and `NEWKEYS`.
- Observed that subsequent SSH packets were encrypted.

## Key Findings
Verifying the host-key fingerprint helps prevent impersonation. SSH negotiates fresh session keys before protecting later communication.