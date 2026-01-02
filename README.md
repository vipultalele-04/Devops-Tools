# Devops-Tools

A collection of DevOps automation scripts for system monitoring and infrastructure management.

## Tools Available

### 1. System Monitoring
Automated monitoring script that tracks CPU, RAM, and storage usage with email alerts.

**Features:**
- CPU, RAM, and storage monitoring
- Configurable thresholds (default: 80%)
- Email alerts via Gmail SMTP
- Real-time system status reporting

[View Documentation](System-monitoring/README.md)

### 2. Process and Port Monitoring
Monitors system processes and port usage with automated email notifications.

**Features:**
- Process status monitoring
- Port availability checking
- Email alerts for issues
- Customizable process and port configuration

[View Documentation](process-and-port-monitoring/README.md)

## Quick Start

```bash
# System Monitoring
chmod +x System-monitoring/system-monitoring.sh
./System-monitoring/system-monitoring.sh

# Process and Port Monitoring
chmod +x process-and-port-monitoring/process-and-port-monitoring.sh
./process-and-port-monitoring/process-and-port-monitoring.sh
```

## Requirements
- Linux/Unix system with bash
- `curl` for email notifications
- Gmail account with app password

## Maintainer
talelevipul5@gmail.com