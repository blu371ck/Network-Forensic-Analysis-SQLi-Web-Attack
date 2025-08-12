# Network Forensic Analysis SQLi Web Attack

## Objective Summary
This report provides a detailed forensic analysis of a multi-stage web application attack targeting an e-commerce platform. The investigation, based on network traffic (PCAP) analysis, traces the threat actor's complete attack chain: from initial reconnaissance and SQL injection to customer data exfiltration and the establishment of persistence via a PHP web shell. The document breaks down the attacker's techniques, provides key indicators of compromise (IOCs), maps actions to the MITRE ATT&CK framework, and concludes with a comprehensive remediation and hardening plan.

## Key Highlights
- __End-to-End Attack Analysis__: Deconstructs the full lifecycle of the intrusion, from initial directory fuzzing to post-exploitation persistence.
- __SQL Injection (SQLi) Deep Dive__: Identifies and explains the attacker's use of both boolean-based and UNION-based SQLi techniques to confirm the vulnerability and exfiltrate data from the `customers` table.
- __Privilege Escalation and Persistance__: Details how the attacker leveraged compromised credentials to authenticate to an admin panel and upload a PHP reverse shell, gaining persistent command-line access to the server.
- __Evidence-Based Findings__: All conclusions are directly supported by evidence extracted from network traffic captures, including specific URIs, malicious payloads, and server responses.
- __Actionable Intelligence__: The report translates technical findings into actionable intelligence, providing specific IOCs for immediate blocking and three-tiered strategic plan for containment, remediation, and future prevention.