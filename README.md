# Bash-Monitoring-Tool 

The monitor project is a custom-built system monitoring script designed to track key system metrics such as CPU usage, memory consumption, and disk usage. The project features real-time monitoring, email notifications for critical states, and weekly system reports. This solution is built using Bash scripting, giving it flexibility and the ability to run in any Linux environment.

This document outlines the key aspects of the project, including setup, usage, configuration, and troubleshooting, along with insights into how the system was customized to meet the challenge requirements.

## Features
### Real-Time Metrics Monitoring: 
Collects CPU, memory, and disk usage.
### Critical Alerts:
Sends email notifications if system resources exceed set thresholds.
### CSV Logging:
Saves system metrics to a CSV file for later analysis.
### Weekly Reports:
Sends a detailed system report via email every week.
### Customizable:
Easily change the critical thresholds and email notifications.


## Installation Instructions
### Prerequisites
Before running the monitoring tool, ensure the following dependencies are installed:

#### msmtp:
A simple SMTP client used to send email notifications.
#### Cron:
For scheduling the script to run at regular intervals.
#### Install msmtp
sudo apt install msmtp
