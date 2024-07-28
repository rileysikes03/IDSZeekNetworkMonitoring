# Network Monitoring with Snort and Zeek

## Objective

In this project, I will set up and configure Snort and Zeek to monitor network traffic. By integrating these tools, I aim to effectively analyze and secure network environments, gaining valuable insights into potential threats and malicious activities.

## Tools Introduced

- **Snort**: An open-source Intrusion Detection System (IDS) that performs real-time traffic analysis and packet logging. It utilizes a rule-based language to detect various types of network attacks.
- **Zeek**: Formerly known as Bro, Zeek is a powerful network analysis framework that logs network traffic into categorized files, providing detailed insights into network behavior.

## Installation and Configuration

```bash
# Update System
sudo apt update
sudo apt upgrade

# Install Snort
sudo apt install snort

# Configure Snort
sudo nano /etc/snort/snort.conf
# (Define your network settings, such as the HOME_NET variable to match your network range.)

# Test Snort Configuration
sudo snort -T -c /etc/snort/snort.conf

# Start Snort
sudo systemctl start snort

# Verifying Output for Snort
sudo tail -f /var/log/snort/alert

# Install Zeek
sudo apt install zeek

# Configure Zeek
sudo nano /opt/zeek/etc/node.cfg
# (Ensure Zeek is set to monitor the correct network interface.)

# Start Zeek
sudo zeekctl deploy

# Verifying Output for Zeek
sudo ls /opt/zeek/logs/current/

```
## Conclusion

By setting up Snort and Zeek, you can establish a robust network monitoring environment. Snort provides intrusion detection capabilities through real-time analysis and logging, while Zeek offers detailed traffic analysis with categorized logs. Together, these tools enhance your ability to monitor, detect, and respond to network threats effectively.

Screenshots:
<br />
<br />
![Capture1](https://github.com/user-attachments/assets/3ac577d9-46dd-425b-a4df-31c75c57440f)
<br />
Snort being installed
<br />
<br />
![Capture2](https://github.com/user-attachments/assets/c35cb314-33d6-4d8a-a700-7b0636c2ccec)
<br />
Zeek being installed


