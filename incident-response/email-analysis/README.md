# Phishing Email Incident Response – Header Analysis

## Overview
This lab documents the analysis of a suspected phishing email impersonating a legitimate brand. The investigation focused on **email header analysis** and **embedded URL behavior** to assess malicious intent.

## Email Summary
- **Email Type:** Phishing (Credential Harvesting)  
- **Attack Vector:** Email  
- **Impersonated Brand:** Coinbase  
- **User Impact:** Risk of account compromise  

## Tools Used
- **MXToolbox** – Email header analysis  
- **urlscan.io** – URL behavior analysis  
- **VirusTotal** – Domain and URL reputation  
- **Manual Inspection** – Email content and header review  

## Analysis Performed
- Reviewed sender address and email content  
- Analyzed SPF authentication results  
- Investigated embedded URL behavior  
- Checked URL and domain reputation using VirusTotal  
- Identified social engineering techniques present in the message  

## Key Findings
- Sender domain **not associated with Yahoo**  
- **SPF authentication failed** for the sending IP address  
- Embedded URL redirected to an **obfuscated third-party domain** unrelated to Yahoo  
- VirusTotal flagged the domain as **suspicious/malicious** based on vendor detections  
- Email relied on **urgency and fear-based social engineering**  
- Landing page behavior appeared designed to **evade automated detection**  

## Verdict
This email is classified as **malicious phishing** based on:  
- Authentication failures  
- Domain impersonation  
- Deceptive URL behavior  
- Corroborating threat intelligence from VirusTotal  

## Mitigation Actions
- Block the sender domain and associated IP addresses  
- Remove the email from affected inboxes  
- Educate users on common phishing indicators  
- Monitor for similar phishing campaigns  

## Data Handling & Redaction
- All email headers, IP addresses, message IDs, and recipient identifiers have been **partially redacted** to protect user privacy while preserving forensic value  

## Indicator Sanitization (Defanging)
- All URLs and domains in this report have been **defanged** (e.g., `example[.]com`) to prevent accidental execution  
- This is a standard incident response practice for safely sharing **Indicators of Compromise (IOCs)** in public repositories  

## Evidence
[All supporting evidence and analysis artifacts for this incident are maintained in the findings directory.
](https://github.com/fortjessica/Cybersecurity-Projects/tree/0ffe53276d372bcacbcc3e519e3eb246022f58b4/incident-response/email-analysis/findings)
