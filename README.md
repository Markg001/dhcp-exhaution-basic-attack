# DHCP Starvation Attack Script

This Python script performs a **DHCP Starvation Attack**, designed to exhaust a DHCP server's IP address pool by sending continuous DHCP discovery packets with random MAC addresses. The attack prevents legitimate devices from obtaining IP addresses, disrupting network services.

---

## How It Works
The script leverages the **Scapy** library to create and send DHCP discovery packets. Each packet includes:
- **Random MAC Address**: Simulates unique clients.
- **Broadcast IP Address**: Targets the DHCP server (`255.255.255.255`).
- **Source IP Address**: Set to `0.0.0.0`, indicating the client is requesting an IP.

The attack runs continuously in a loop to overwhelm the DHCP server.

---

## Requirements

1. **Python 3.6+**
2. **Scapy Library**: Install it using:
   ```bash
   pip install scapy
   ```

