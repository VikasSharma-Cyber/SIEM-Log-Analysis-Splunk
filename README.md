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

Brute Force Detection
index=main "failed password"
| stats count by src_ip
| where count > 5
| sort -count

Top Source IPs
index=main| top src_ip

Successful Login Detection
index=main "Accepted password"
| stats count by user
| sort -count


