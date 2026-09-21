# Day 01: Lab Architecture & Network Diagram
## 🎯 Objectives
Define the architecture and data flow for the Home SOC Automation Lab.

Map out endpoint telemetry collection, SIEM processing, SOAR automation, and case management.

## 🏗️ Architecture & Data Flow Diagram

<img width="805" height="760" alt="Untitled Diagram" src="https://github.com/user-attachments/assets/f078569b-522f-4ae7-9f6e-7a69b25f6bf8" />


## 🔄 End-to-End Workflow Breakdown:
Step 1 (Send Events): The Windows 10 Client (Wazuh Agent) generates and transmits security telemetry through the router/internet[cite: 2].

Step 2 (Receive Events): Wazuh Manager receives, processes, and evaluates the incoming endpoint events[cite: 2].

Step 3 & 4 (Send Alerts & Enrich IOCs): Wazuh triggers alerts to Shuffle (SOAR), which then queries external services for OSINT data enrichment[cite: 2].

Step 5 (Send Alerts): Shuffle forwards structured alerts and case data to TheHive for incident case management[cite: 2].

Step 6 & 7 (Communication): Shuffle integrates with email services to notify the SOC Analyst[cite: 2].

Step 8 (Response Action): The SOC Analyst or automated Shuffle playbook executes containment and response actions back down to the Windows 10 Client[cite: 2].

## 🛠️ Components Deployed
Endpoint: Windows 10 Client running the Wazuh Agent[cite: 2].

SIEM / EDR: Wazuh Manager (Cloud/Server)[cite: 2].

SOAR / Automation: Shuffle platform integrated with OSINT tools[cite: 2].

Case Management: TheHive for ticketing and tracking[cite: 2].

Analyst Workstation: SOC Analyst interface for monitoring and responding[cite: 2].

