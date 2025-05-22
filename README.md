# ARP Spoofing and Detection

This project demonstrates an ARP spoofing attack and detection script, where the attacker positions themselves as a Man-in-the-Middle (MITM) by exploiting the ARP (Address Resolution Protocol) mechanism.

---

## 🧠 Overview

ARP spoofing is a reliable method for executing MITM attacks by sending falsified ARP messages over a local network. This causes the victim to associate the attacker's MAC address with the IP address of the gateway or another device, allowing the attacker to intercept network traffic.

---

## 🛠️ Setup

### System Roles

- **Attacker Machine:** Windows  
- **Victim Machine:** Kali Linux  

> ⚠️ Since the attacker machine is Windows, any libraries or tools used must be compatible with Windows. For example, `scapy` is commonly used for packet manipulation but may not work natively on Windows without proper setup.

---

## 📦 Installing Scapy on Windows

To install Scapy on Windows, use one of the following commands:


pip install scapy
C:\python\python.exe -m pip install scapy
##  Running the ARP Spoofing Script

1. Open **Command Prompt** on your Windows machine.
2. Navigate to the directory containing your script. (In this case, the `ARP_spoofer` repository.)
3. Run the script using the following format:


C:\python\python.exe arp_spoof.py

# ARP Spoofing Detection Tool

This Python script detects ARP spoofing attempts on your local network using the Scapy library.

## How It Works

- It continuously sniffs ARP packets on the specified interface.
- For each ARP reply (opcode 2), it compares the actual MAC address of the IP (`get_mac()`) with the MAC address in the ARP reply.
- If they don't match, it prints a warning: **"You are under attack"**.


** Kindly note this is for educational purposes only**
