# DevOps Tools

A collection of DevOps automation scripts and tools for system monitoring and infrastructure management.

## System Monitoring

### Overview
Automated system monitoring script that tracks CPU, RAM, and storage usage with email alerts when thresholds are exceeded.

### Features
- **CPU Monitoring**: Tracks CPU usage and alerts when above 80%
- **RAM Monitoring**: Monitors memory usage with configurable thresholds
- **Storage Monitoring**: Checks disk usage for root partition
- **Email Alerts**: Sends notifications via Gmail SMTP when thresholds are breached
- **Real-time Reporting**: Displays current system status

### Prerequisites
- Linux/Unix system with bash
- `curl` command available
- Gmail account with app password configured

### Configuration
Edit the following variables in `System-monitoring/system-monitoring.sh`:

```bash
CPU_THRESHOLD=80        # CPU usage threshold (%)
RAM_THRESHOLD=80        # RAM usage threshold (%)
STORAGE_THRESHOLD=80    # Storage usage threshold (%)
EMAIL_ID="your-email@gmail.com"
APP_PASSWORD="your-app-password"
```

### Usage
```bash
chmod +x System-monitoring/system-monitoring.sh
./System-monitoring/system-monitoring.sh
```

### Automation
Add to crontab for regular monitoring:
```bash
# Run every 5 minutes
*/5 * * * * /path/to/system-monitoring.sh
```

## Maintainer
- Email: talelevipul5@gmail.com

## License
Open source - feel free to modify and distribute.