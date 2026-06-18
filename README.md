# SOC Security Monitoring Dashboard

A beginner-friendly **Security Operations Center (SOC) dashboard** built with **Splunk Cloud** to monitor, analyze, and visualize security events using **Search Processing Language (SPL)**.

This project demonstrates core SIEM skills used by SOC analysts, including log analysis, dashboard creation, event monitoring, and data visualization.

---

## Dashboard Overview

This dashboard contains the following security monitoring panels:

- Total Events
- Events by Sourcetype
- Top Hosts
- Event Trend
- Events by Index
- Recent Events

---

## Technologies Used

- Splunk Cloud
- Splunk Search Processing Language (SPL)
- Security Information and Event Management (SIEM)
- Log Analysis
- Security Monitoring
- Dashboard Visualization
- Data Analysis
- Cybersecurity

---

## Skills Demonstrated

- Splunk Dashboard Development
- SPL Query Writing
- SIEM Monitoring
- Security Event Analysis
- Threat Monitoring
- Log Investigation
- Host Analysis
- Sourcetype Analysis
- Event Trend Analysis
- Dashboard Visualization
- Security Reporting

---

## SPL Queries

### Total Events

```spl
index=*
| stats count
```

### Events by Sourcetype

```spl
index=*
| stats count by sourcetype
| sort -count
```

### Top Hosts

```spl
index=*
| stats count by host
| sort -count
```

### Event Trend

```spl
index=*
| timechart count
```

### Events by Index

```spl
index=*
| stats count by index
```

### Recent Events

```spl
index=*
| table _time host sourcetype source
| sort -_time
```

---

## Dashboard Preview

### Dashboard Overview

![Dashboard Overview](Dashboard%20Overview.png)

### Event Trend

![Event Trend](Event%20Trend.png)

### Recent Events

![Recent Events](Recent%20Events.png)

---

## What I Learned

Throughout this project I learned how to:

- Navigate Splunk Cloud
- Write SPL searches
- Build SIEM dashboards
- Analyze log data
- Monitor hosts and event sources
- Visualize security information
- Investigate security events
- Create dashboard panels
- Organize security data for analysis

---

## Future Improvements

- Windows Security Event Log Monitoring
- Sysmon Log Integration
- Linux Authentication Log Analysis
- Failed Login Detection
- Brute Force Detection
- PowerShell Activity Monitoring
- Threat Intelligence Integration
- MITRE ATT&CK Mapping
- Security Alert Automation
- Email Notifications

---

## Author

**Darwin Brown**
