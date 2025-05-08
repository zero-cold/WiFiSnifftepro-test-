WiFiSniffPro
WiFiSniffPro is an ethical Wi-Fi security testing tool designed for Kali Linux. It allows users to scan wireless networks, capture WPA/WPA2 handshakes, send deauthentication packets, and generate reports. The tool features a professional GUI built with PyQt5.
WARNING: This tool is for ethical hacking and security testing purposes only. Unauthorized use on networks you do not own or have explicit permission to test is illegal and may result in severe legal consequences.
Features

Scan Wi-Fi networks and display SSID, BSSID, encryption type, and signal strength.
Capture WPA/WPA2 handshakes and save them as .cap files for analysis with tools like Aircrack-ng.
Send deauthentication packets to facilitate handshake capture.
Filter networks by encryption type (WEP, WPA, WPA2, Open).
Save scan results as CSV reports.
User-friendly GUI with PyQt5.

Requirements

Operating System: Kali Linux (latest version recommended).
Hardware: Wi-Fi adapter supporting monitor mode and packet injection (e.g., Alfa Network AWUS036NHA).
Software:
Python 3
Scapy
PyQt5
Aircrack-ng (for handshake analysis, optional)



Installation

Clone the repository:git clone https://github.com/yourusername/WiFiSniffPro.git
cd WiFiSniffPro


Install dependencies:sudo pip install -r requirements.txt


Ensure Aircrack-ng is installed:sudo apt update
sudo apt install aircrack-ng


Verify your Wi-Fi adapter supports monitor mode:iwconfig



Usage

Run the tool with root privileges:sudo python3 wifisniffpro.py


Enter your network interface name (e.g., wlan0).
Click "Start Scan" to discover nearby Wi-Fi networks.
Select a network from the table to target it.
Click "Send Deauth" to send deauthentication packets and capture the handshake.
Handshakes are saved in the captures/ directory.
Click "Save Report" to export scan results as a CSV file.

Example
To analyze a captured handshake with Aircrack-ng:
aircrack-ng -w wordlist.txt -b [BSSID] captures/handshake_[BSSID]_[timestamp].cap

Legal Disclaimer
WiFiSniffPro is intended for security researchers and ethical hackers with explicit permission to test networks. Using this tool on networks without authorization is illegal and punishable by law. The developers are not responsible for any misuse.
License
This project is licensed under the MIT License. See the LICENSE file for details.
Contributing
Contributions are welcome! Please submit a pull request or open an issue on GitHub.
Contact
For questions or feedback, please open an issue on the GitHub repository.
