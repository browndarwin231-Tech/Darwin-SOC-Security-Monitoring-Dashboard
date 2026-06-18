# SOC Security Monitoring Dashboard

A beginner-friendly Security Operations Center (SOC) dashboard built with Splunk Cloud.

This project demonstrates how security analysts monitor log activity, visualize security events, and investigate systems using Splunk dashboards.

---

## Dashboard Overview

The dashboard includes:

- Total Events
- Events by Sourcetype
- Top Hosts
- Event Trend (Last 24 Hours)
- Events by Splunk Index
- Recent Events

---

## Technologies Used

- Splunk Cloud
- SPL (Search Processing Language)
- SIEM Concepts
- Log Analysis
- Dashboard Visualization

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
| sort - count
```

### Top Hosts

```spl
index=*
| stats count by host
| sort - count
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
| head 10
```

---

## Skills Demonstrated

- SIEM Monitoring
- Splunk Dashboard Development
- SPL Query Writing
- Security Event Analysis
- Log Investigation
- Dashboard Visualization
- SOC Workflow

---

## What I Learned

- Building dashboards in Splunk Cloud
- Writing SPL searches
- Monitoring event activity
- Analyzing hosts and sourcetypes
- Organizing SOC dashboards
- Visualizing security data

---

## Dashboard Preview

### Dashboard Overview

![Dashboard Overview](Dashboard%20Overview.png)

### Event Trend

![Event Trend](Event%20Trend.png)

### Recent Events

![Recent Events](Recent%20Events.png)
