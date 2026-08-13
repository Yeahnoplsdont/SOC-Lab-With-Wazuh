
What is a SIEM?
  -Endpoints, firewalls, and routers all generate logs, and a SOC analyst's job is to catch indicators of compromise (IoCs) in that data. Checking each log source individually doesn't scale. A SIEM solves this by aggregating logs into one place and normalizing them into a common format, correlating events across sources, and applying rules to surface alerts and turning raw log volume into something an analyst can actually act on.
  
What is Wazuh?
  -Wazuh is an open-source SIEM/XDR platform. Agents installed on endpoints forward log data (event logs, syslog, Sysmon telemetry, etc.) to a central manager, which decodes and matches that data against a rule, some rules match single suspicious events, others fire on frequency/thresholds, and some generate alerts. Beyond core SIEM functions, Wazuh also handles file integrity monitoring (FIM), vulnerability detection, and configuration/compliance assessment.

Day 3 notes
I have worked through the full lifecycle of account activity end to end. I created, elevated, and deleted a local account, enabled a disabled guest account and triggered failed and successful SSH login, ran recon/exfil-style commands like cat /etc/passwd. Then traced every action back to its source in the SIEM 
