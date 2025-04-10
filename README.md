# Frio

Frio is a Raspberry Pi Zero 2 W-based Wi-Fi deauther and handshake capturer built from scratch using raw sockets and low-level C code for maximum control and efficiency.

⚠️ **This project is strictly for educational and research purposes. I do not condone or take responsibility for any malicious use.**

---

## Features

- 📡 **Deauthentication** using custom-built C code with raw packet injection.
- 🔎 **EAPOL Handshake Sniffer** built on top of `libpcap` for efficient packet capture.
- 💾 **Handshake Dumper** to easily export captured credentials.
- 📺 **Display Manager** using either a 20x4 I2C LCD or OLED to show live status.
- 🔘 **GPIO Trigger** to kill daemons, switch to managed mode, and start SSH daemon for file transfers.
- 💻 **SCP Integration** for secure file transfers to a PC after capture.

---

## Workflow

1. **Deauth** a target access point to force devices to reconnect.
2. **Sniff** for EAPOL packets and capture WPA handshakes.
3. **Display** current target info, channel, and capture state.
4. On **button press**, stop all daemons, switch to managed mode, enable SSH, and display IP.
5. **SCP** handshake files from the Pi to your main machine.

---

## Tech Stack

- Raspberry Pi Zero 2 W
- C (Raw sockets + pcap)
- C(initial display manager)
- I2C LCD / OLED for display
- Bash for utility scripts

---

## Legal Disclaimer

This tool is intended for authorized testing and research purposes only. Unauthorized access to networks is illegal and unethical. Use responsibly.

---
