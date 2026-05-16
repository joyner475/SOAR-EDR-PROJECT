# SOAR-EDR-PROJECT

## Objective

The objective of this project is to design, implement, and operationalize a simple Security Orchestration, Automation, and Response (SOAR) solution integrated with Endpoint Detection and Response (EDR) and Security Information and Event Management (SIEM) capabilities. This initiative will leverage LimaCharlie, Splunk, and Tines to significantly enhance threat detection, accelerate incident response, and strengthen the overall cybersecurity resilience of my created lab organization.

### Skills Learned
   ### Technical skills
- intergration of multiple security tools (limacharlie + splunk + tines) to create a unified security operation pipeline
- Development of automated incident response playbooks for common and high-severity threats (malware, ransomware, lateral movement, credential abuse)
- Alert enrichment, false positive reduction, and intelligent decision-making through automation.
- API integrations and webhook configurations between EDR, SIEM, and SOAR platforms.
  ### Incident response skills
- Real-time threat detection, investigation, and containment on endpoints
- Creation and optimization of custom detection rules in LimaCharlie
- Proactive threat hunting techniques using EDR telemetry and SIEM data
  ### Proffessional security operation skills
- Real-time monitoring, metrics tracking, and executive-level reporting using Splunk and Tines dashboards.
- Slack-based security alerting and team collaboration workflows.

### Tools Used

- Security Information and Event Management (SIEM) system (Splunk) for log ingestion and analysis.
- A cloud based SecOp EDR platform (Limacharlie) for log management and endpoint detections.
- A SOAR and wrokflow automation platform ( Tines ) for sending alerts and isolating infected machines
## Steps
## Step1
## Creating the playbook workflow
<img width="1540" height="949" alt="Screenshot 2026-05-15 105532" src="https://github.com/user-attachments/assets/8215b4e7-c98c-45c8-b531-92f1fe55cf5d" />
Ref1: the SOAR-EDR playbook workflow diagram
## Step2

## Installing and setting up Limacharlie in windows server.
- head over to google and signup your new account in Limacharlie.com
- create your new organization
- click the created organization and click the installation key tab to create your installation key
- copy the sensor key and head to sensors list to download an EDR (windows). ensure you copy the windows link to the server to download the agent.
- in the server, head to downloads and open powershell with admin priviledges. install the HCP agent using hcp(tab) -i [copied sensor key]

    <img width="1857" height="795" alt="Screenshot 2026-05-15 110430" src="https://github.com/user-attachments/assets/f0f47bda-48f8-42c0-af69-a8f5a1824207" />
Ref2: limacharlie dashboard
## step3

## Generating Telemetry using Lazage(credential recovery hacktool)
## Creating a Dtection and Response rule
<img width="1539" height="502" alt="Screenshot 2026-05-16 110116" src="https://github.com/user-attachments/assets/bc77c3b1-007b-4157-b6dc-d484c4724971" />
Ref3: creating a Rule in limacharlie

## Step3
  ## Setting up slack and tines

  ## Slack 
  <img width="1916" height="885" alt="Screenshot 2026-05-16 115316" src="https://github.com/user-attachments/assets/a6b18862-a4ad-4aed-99a7-4918a55b2fc6" />
 Ref4: slack dashboard with a channel "Edr-alerts"

  ## Tines
 <img width="1919" height="906" alt="Screenshot 2026-05-16 120606" src="https://github.com/user-attachments/assets/8a6e9939-1af3-4d69-ba69-6872cd1d2133" />

Ref5: Tines dashboard with a new created story

## Step4
  ## Testing the connection between Tines and Limacharlie
  <img width="1919" height="962" alt="Screenshot 2026-05-16 120844" src="https://github.com/user-attachments/assets/51a06a4d-8561-4535-a03b-e0182c5d482b" />
Ref6: connected tines with limacharlie using a webhook

## Step5
  ## Sending a slack message
  <img width="1899" height="877" alt="Screenshot 2026-05-16 124124" src="https://github.com/user-attachments/assets/0f74a75e-eb4e-4739-95e9-42f9665a9970" />
Ref7: received an alert message from slack 

  ## Sending an email
  <img width="1919" height="899" alt="Screenshot 2026-05-16 124711" src="https://github.com/user-attachments/assets/ff6f7e87-cfd3-4859-98bd-2fd1f3f2d917" />
Ref8: Sending an alert email 

  ## Generating a user Prompt
<img width="1526" height="877" alt="Screenshot 2026-05-16 132528" src="https://github.com/user-attachments/assets/d0fb5c9c-b362-4fe1-abac-ef41254a6805" />
Ref9: configuring the prompts to Isolate the machine
