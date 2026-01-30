# Phishing Email Incident Response – Header Analysis

## Overview
This lab documents the analysis of a suspected phishing email impersonating a legitimate brand. The investigation focuses on email header analysis and embedded URL behavior to determine malicious intent.

## Email Summary
- **Email Type:** Phishing (Credential Harvesting)  
- **Attack Vector:** Email  
- **Impersonated Brand:** Coinbase  
- **User Impact:** Risk of account compromise  

## Tools Used
- **MXToolbox** – Email header analysis  
- **urlscan.io** – URL behavior analysis  
- **VirusTotal** – Domain and URL reputation analysis  
- **Manual inspection** – Content and header review  

## Analysis Performed
- Reviewed sender address and email content  
- Analyzed SPF authentication results  
- Investigated embedded URL behavior  
- Checked URL and domain reputation using VirusTotal  
- Identified social engineering techniques used in the message  

## Key Findings
- Sender domain was not associated with Yahoo  
- SPF authentication failed for the sending IP address  
- Embedded URL redirected to an obfuscated third-party domain unrelated to Yahoo  
- VirusTotal flagged the domain as suspicious/malicious based on vendor detections  
- Message relied on urgency and fear-based social engineering  
- Landing page behavior appeared designed to evade automated detection  

## Verdict
This email was classified as **malicious phishing** based on authentication failures, domain impersonation, deceptive URL behavior, and corroborating threat intelligence from VirusTotal.

## Recommended Response
- Block the sender domain and associated IP addresses  
- Remove the email from affected inboxes  
- Educate users on common phishing indicators  
- Monitor for similar phishing campaigns  

## Data Handling & Redaction
All email headers, IP addresses, message IDs, and recipient identifiers have been partially redacted to protect user privacy while preserving forensic value.

## Indicator Sanitization (Defanging)
All URLs and domains in this report have been intentionally defanged (e.g., `example[.]com`) to prevent accidental execution.  
This is a standard incident response practice for safely sharing indicators of compromise (IOCs) in public repositories.

## Evidence
[Artifacts related to this incident are stored in the] (incident-response/email-analysis/findings)
