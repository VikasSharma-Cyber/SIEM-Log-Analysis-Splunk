# SIEM-Log-Analysis-Splunk
SIEM project using Splunk for log analysis and threat detection.
# SIEM Log Analysis & Threat Detection using Splunk

## Overview
This project is based on SIEM log analysis using Splunk. It helps detect failed login attempts, brute-force attacks, and suspicious IP activity.

## Tools Used
- Splunk
- SPL
- Linux Logs
- Dashboards
- Alerts

## Features
- Log analysis
- Failed login detection
- Brute-force detection
- Dashboard creation
- Alert generation

## SPL Queries

### Failed Login Detection
```spl
index=main "failed password"
| stats count by src_ip
| sort -count
