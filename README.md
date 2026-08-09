# SOC-Lab-With-Wazuh

-This repo will be my documentation for my progress through a free, hands-on SOC analyst challenge: building an on-prem detection lab with Wazuh from scratch, generating my own telemetry, writing my own detection rules, and completing a full investigation. I'm using this README as a running log of what I built, what broke, and what I actually learned at each stage so I can use for my own reference, and partly as something I can point to when I talk about this project.

Lab Environment
   -SIEM/XDR platform: Wazuh
   -VMs: 3 running simultaneously (Wazuh manager + Windows endpoint + Linux endpoint)
   -Host resources: 16–32 GB RAM recommended for running everything locally
   
What is a SIEM?
 - An Endpoint, firewall, and router all have something in common. That is they all generate logs, a SOC analysts job is to monitor alerts for any indicators of compromise however, the problem is that it is difficult to look at each of those IoT individually, the solution? A SIEM. 

What is Wazuh?
   - A SIEM aggregates logs into 1 space so the SOC analyst uses daily to be able to see all the logs in one place.
   - Wazuh is a SIEM that monitors endpoints and fires alerts when thresholds are crossed based on rules that are set up.

