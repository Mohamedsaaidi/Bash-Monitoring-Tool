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


### How secure is the email authentication process?
Bash tool uses an App Password generated specifically for the Gmail account. This ensures your primary account password remains secure.

Additionally, it is strongly recommended to store the App Password in an environment variable to avoid exposing it in the code.

### What does the monitor project do?

The monitor project is a custom system monitoring tool that tracks CPU, memory, and disk usage on a Linux machine. It sends email alerts for critical states, logs metrics in a CSV file, and generates weekly system reports.

### Why build this tool instead of using existing monitoring solutions?
The project aims to provide hands-on experience in scripting and system monitoring. It also allows for full customization of features, thresholds, and functionality to suit specific needs.


### How do I run the monitoring script manually?
 
 Use the following command to execute the script: 
 ./monitor.sh

### How do I generate a weekly report?

 Run the script with the --weekly-report flag:
 ./monitor.sh --weekly-report

## Troubleshooting

#### I’m not receiving email notifications. What should I do?

Verify by : cat ~/.msmtp.log
and : sudo tail -f /var/log/mail.log


#### The script gives a “Permission Denied” error. How can I fix it?

chmod +x monitor.sh

## Other questions

#### Can I add more metrics to monitor?

Yes, you can modify the script to collect additional system data, such as network bandwidth, I/O performance, or system load.

#### How do I view the CSV file data?

Open system_metrics.csv using a text editor or spreadsheet software like LibreOffice Calc or Excel.

#### Can I make the script interactive?

Yes, you can use tools like dialog or Python libraries such as curses to build an interactive interface for the script.


 














