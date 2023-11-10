# Postmortem

## **Issue Summary**

- **Start time**: November 7, 2023, 10:00 AM (GMT)
- **End time**: November 7, 2023, 12:30 PM (GMT)
- **Duration**: 2.5 hours
- **Impact**: Approximately 35% of users experienced slow response times or timeouts.
- **Root cause**: Misconfiguration in the database's memory allocation settings.

## **Timeline**

- **10:00 AM**: Issue detected by automated monitoring system.
- **10:15 AM**: Initial investigation suspected a network issue.
- **10:45 AM**: Network checks performed, no issues found.
- **11:00 AM**: Database logs showed memory allocation errors, issue escalated to database team.
- **11:30 AM**: Misconfiguration in memory settings identified.
- **12:00 PM**: Misconfiguration corrected, database restarted.
- **12:30 PM**: System returned to normal operation.

## **Root Cause and Resolution**

The root cause of the issue was a misconfiguration in the database's memory allocation settings. This was inadvertently introduced during a recent update. The database was trying to allocate more memory than was available, causing it to slow down and occasionally crash. The issue was resolved by correcting the memory allocation settings and restarting the database.

## **Corrective and Preventive Measures**

- Implement stricter change control processes for database configuration changes.
- Improve our monitoring to catch memory-related issues sooner.
- Provide additional training to our engineers on database configuration and troubleshooting.
- Review and update our database configuration based on the vendor's best practices.

