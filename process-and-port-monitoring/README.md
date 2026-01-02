# Process and Port Monitoring Script

A bash script that monitors system processes and port usage, sending email alerts when issues are detected.

## Features

- Monitors specified process status
- Checks if specific ports are in use
- Sends email notifications via Gmail SMTP

## Configuration

Edit the following variables in the script:

```bash
PROCESS_NAME="bash"          # Process to monitor
PORT_NUMBER="80"             # Port to monitor
EMAIL_ID="your@gmail.com"    # Gmail address
APP_PASSWORD="xxxx xxxx xxxx xxxx"  # Gmail app password
```

## Gmail App Password Setup

1. Enable 2-Factor Authentication on your Gmail account
2. Go to Google Account > Security > 2-Step Verification > App passwords
3. Generate an app password for "Mail"
4. Use this password in the script

## Usage

```bash
chmod +x process-and-port-monitoring.sh
./process-and-port-monitoring.sh
```

## What the Script Executes

1. **Process Check**: Uses `ps aux` to verify if the specified process is running
   - If running: Logs success message
   - If not running: Sends email alert

2. **Port Check**: Uses `netstat -tuln` to check if the specified port is in use
   - If in use: Logs success message
   - If not in use: Sends email alert

3. **Email Notification**: Uses `curl` with Gmail SMTP to send alerts via email when issues are detected

## Requirements

- `curl` - for sending emails
- `netstat` - for port monitoring
- `ps` - for process monitoring

## Alerts

The script sends email alerts when:
- The monitored process is not running
- The monitored port is not in use

## Maintainer

talelevipul5@gmail.com
