# TLS 1.3 – Handshake Analysis

## Objective
Understand the TLS 1.3 handshake, key establishment, and server authentication by examining a packet capture.

## Tools & Technologies
Wireshark, TLS 1.3, TLS key log file.

## Implementation & Analysis
- Inspected ClientHello, ServerHello, supported cipher suites, and the `key_share` extension.
- Loaded a TLS key log file to examine encrypted handshake messages.
- Examined the certificate chain and discussed how the server proves possession of its private key.
- Compared TLS 1.3's 1-RTT handshake and compatibility ChangeCipherSpec messages with older TLS behavior.

## Key Findings
TLS 1.3 encrypts most handshake messages after ServerHello. The key log enabled inspection of messages otherwise hidden in the capture; certificates and CertificateVerify support server authentication.