
# Snort Network Intrusion Detection System (NIDS)

## Overview
Snort is an open-source network intrusion detection system (NIDS) capable of real-time traffic analysis and packet logging. This repository provides a guide on installing and configuring Snort for effective intrusion detection.


## Installation
## Prerequisites
- Linux Operating System (e.g., Ubuntu, CentOS)
- Compiler Tools (gcc, make, etc.)
- libpcap Library

## Steps
1. Update Package Lists :

```bash
sudo apt update
```
2. Install Snort :
```bash
sudo apt install snort
```
3. Configure Snort :

Edit the main config file :
```bash
sudo nano /etc/snort/snort.conf
```
4. Test Configuration :
```bash
sudo snort -T -c /etc/snort/snort.conf
```
## Usage
1. Start Snort :
```bash
sudo systemctl start snort
```
2. Check Status :
```bash
sudo systemctl status snort
```
3. Automatically Start on Boot :
```bash
sudo systemctl enable snort
```
4. View Alerts :
```bash
sudo less /var/log/snort/alert
```

## Additional Steps
1. Download Community Rules :
```bash
sudo wget https://www.snort.org/rules/community -O /etc/snort/community.rules
```
2. Generate Test Traffic :
```bash
sudo snort -A console -q -c /etc/snort/snort.conf -i eth0
```

## That's it! Your Snort NIDS is now set up and ready to detect any suspicious network activity.
## Features
- Real-time network traffic analysis
- Customizable rule-based configuration
- Wide range of threat detection: malware, DoS attacks, SQL injections, etc.
- Flexible alerting options: console, logs, email
- Multi-platform support: Linux, BSD, Windows


## Resources

 - [Official Snort Documentation](https://www.snort.org/documents)
 - [Snort Rules Community](https://www.snort.org/faq/what-are-community-rules)

## Author

- [Rahul Sehgal](https://github.com/cyb-sehgal)
