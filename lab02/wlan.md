# Lab 2 – Wireless Network Security

## Objective
Explore weaknesses in WEP and WPA2-PSK and examine authentication mechanisms used in enterprise Wi-Fi networks.

## Tools & Technologies
Kali Linux, Aircrack-ng suite (`airmon-ng`, `airodump-ng`, `aircrack-ng`), Wireshark, WLAN monitor mode.

## Implementation & Analysis

### WEP Security
- Reviewed how monitor mode and the Aircrack-ng tools can be used to capture and analyze wireless traffic.
- Analyzed a provided WEP capture (`NetSecAP1.cap`) with `aircrack-ng` to recover the shared key.
- Examined WEP weaknesses, including IV reuse and vulnerabilities in RC4-based encryption.

### WPA2-PSK Dictionary Attack
- Identified a target access point and captured a WPA handshake using `airodump-ng`.
- Tested password candidates from `password.lst` against the captured handshake using `aircrack-ng`.
- Successfully recovered the lab password, demonstrating the risk of weak pre-shared passwords.

### WPA2/WPA3-Enterprise Authentication (Theory)
- Studied the roles of supplicant, authenticator, and RADIUS authentication server in 802.1X.
- Compared certificate-based EAP-TLS with tunneled EAP methods such as PEAP, focusing on server certificate validation and trust.

## Key Findings
WEP is insecure due to fundamental cryptographic weaknesses. WPA2-PSK can be vulnerable to offline dictionary attacks when weak passwords are used. Enterprise authentication relies on correctly configured EAP methods and trusted authentication servers.
