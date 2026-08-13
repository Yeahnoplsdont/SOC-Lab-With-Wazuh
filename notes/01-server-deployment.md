
What is a SIEM?
  -Endpoints, firewalls, and routers all generate logs, and a SOC analyst's job is to catch indicators of compromise (IoCs) in that data. Checking each log source individually doesn't scale. A SIEM solves this by aggregating logs into one place and normalizing them into a common format, correlating events across sources, and applying rules to surface alerts and turning raw log volume into something an analyst can actually act on.
  
What is Wazuh?
  -Wazuh is an open-source SIEM/XDR platform. Agents installed on endpoints forward log data (event logs, syslog, Sysmon telemetry, etc.) to a central manager, which decodes and matches that data against a rule, some rules match single suspicious events, others fire on frequency/thresholds, and some generate alerts. Beyond core SIEM functions, Wazuh also handles file integrity monitoring (FIM), vulnerability detection, and configuration/compliance assessment.

Day 3 notes
I have worked through the full lifecycle of account activity end to end. I created, elevated, and deleted a local account, enabled a disabled guest account and triggered failed and successful SSH login, ran recon/exfil-style commands like cat /etc/passwd. Then traced every action back to its source in the SIEM and matched the Windows event IDs (4720, 4624, 4726, 4732) to what actually happened on the box, and followed SSH session IDs from login through command execution to logoff on the Linux side. 

I also learned a valuable lesson I learned today account names aren't guaranteed in the logs. Sometimes all you get is a SID/RID, and resolving that back to a real identity is on you not the dashboard and you can only do that if you have the skills to be able to log through the process in the Siem rather than rely on Wazuh to always give you the account name. 

This is important because if you are not able to locate actions and helps you spot fake users, find stolen logins, and stop attacks quickly which are vital to protecting company data and assets from attackers.
