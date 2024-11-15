## Installation Instructions
### Prerequisites
Before running the monitoring tool, ensure the following dependencies are installed:
#### msmtp:
A simple SMTP client used to send email notifications.
#### Cron:
For scheduling the script to run at regular intervals.
#### Install msmtp
sudo apt install msmtp


#### Setup Steps
##### Script: monitor.sh
   
This script collects system metrics and logs them to a CSV file. Each execution appends a new entry to the CSV file with the current date and time, CPU usage, memory usage, and disk usage.

#### Script Contents and Explanation

![text](https://github.com/Mohamedsaaidi/Bash-Monitoring-Tool/blob/main/Instructions/Images/Screenshot%202024-11-15%20at%2013.55.04.png)

#### Configure Msmtp "~/.msmtprc


account default

host smtp.gmail.com

port 587

from your-email@gmail.com

auth on

user your-email@gmail.com

passwordeval "gpg --no-tty -q -d ~/.password.gpg"

tls on

tls_starttls on


#### Set up cron jobs to run the script automatically every hour.
 
 "crontab -e" 
 
0 * * * * /home/mohamed/monitor_project/monitor.sh


0 0 * * SUN /home/mohamed/monitor_project/monitor.sh --weekly-report
 


