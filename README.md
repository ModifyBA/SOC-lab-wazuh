# Mini SOC Lab using Wazuh

## Overview

This project demonstrates a basic Security Operations Center (SOC) built using Wazuh to monitor system activity, detect threats, and analyze security events.

## Objectives

* Build a functional SOC environment
* Simulate real-world attacks
* Detect and analyze suspicious activity
* Visualize security events using dashboards

## Tools Used

* Wazuh (SIEM platform)
* Ubuntu (Linux VM)
* SSH (attack simulation)

## Setup

* Created a virtual machine using VirtualBox
* Installed Ubuntu Linux
* Installed and configured the Wazuh SIEM platform
* Connected system logs to the Wazuh dashboard

## Attack Simulation

Simulated brute-force login attempts using SSH:

```
for i in {1..10}; do ssh -o PreferredAuthentications=none fakeuser@localhost; done
sudo apt install nmap -y
sudo nmap -sS localhost
```

## Detection & Analysis

* Observed authentication failures in the Wazuh dashboard
* Events categorized under MITRE ATT&CK techniques such as:
  * sshd: Attempt to login using a non-existent user
  * Password Guessing
  * Brute Force
* Analyzed logs and timestamps of suspicious activity

## Results

* Successfully detected multiple failed login attempts
* Visualized alerts and patterns in the dashboard
* Demonstrated real-time threat monitoring capability

## Screenshots


<img width="1276" height="803" alt="image" src="https://github.com/user-attachments/assets/995f7ace-b293-49d5-8948-55aeb0b40098" />
<img width="1290" height="801" alt="image" src="https://github.com/user-attachments/assets/b2361e01-6c77-4d9e-bab8-f698fc3d64d7" />

## Key Takeaways

* Learned how SOC environments monitor and detect threats
* Gained hands-on experience with SIEM tools
* Understood how brute-force attacks are identified

## Future Improvements

* Add custom alert rules
* Simulate additional attacks (port scanning, malware behavior)
* Expand monitoring to multiple systems
