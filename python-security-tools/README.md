# Python Security Tools

This folder contains Python scripts and tools I developed while learning penetration testing automation. Inspired by the **"Learn Python & Ethical Hacking From Scratch"** course by Zaid Sabih.

---

## Tools Included

| Script                | Description                                         |
|-----------------------|-----------------------------------------------------|
| `port_scanner.py`     | Custom TCP port scanner with threading support      |
| `network_sniffer.py`  | Packet sniffer to capture and analyze network data  |
| `brute_force_ssh.py`  | Automates SSH brute-force attacks (for lab use only)|
| `keylogger.py`        | Logs keystrokes locally                              |
| `backdoor_client.py`  | Simulates a backdoor client                           |
| `backdoor_server.py`  | Corresponding backdoor server                         |
| `arp_spoofer.py`      | ARP spoofing tool for man-in-the-middle attacks      |

---

## Usage Notes

- These scripts are for **educational use only**.  
- Run them in isolated virtual environments or lab machines.  
- Modify scripts responsibly and understand their ethical implications.

---

## Requirements

- Python 3.x  
- Scapy library (`pip install scapy`)  
- Other standard Python libraries included in the scripts.

---

## Getting Started

Example: Running the port scanner  
```bash
python3 port_scanner.py --target 192.168.1.1 --ports 1-1000
```
