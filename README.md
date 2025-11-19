Phishing URL Analysis — RBF Credit Union (Azure-Hosted Phishing Site)

Status: Completed
Techniques: Credential Harvesting, Brand Impersonation
Tools Used: VirusTotal, URLScan.io, Hybrid Analysis

Overview
This project analyzes a live banking-themed phishing site hosted on Azure infrastructure. The intent of the page is to harvest login credentials by impersonating Randolph Brooks Federal Credit Union (RBF CU).

The URL was taken from public security feeds and analyzed safely using sandbox environments and OSINT tools.

Phishing URL
https://rbfcu-star.azurewebsites.net/(S(r1sza2rk2dwnnl)2ci04ctk))/Main/Login
(Do not open directly — analyze only with sandbox tools.)

VirusTotal Summary
21 / 95 vendors flagged the domain as malicious

Categories: Phishing, Malware, Malicious
Domain age: 14 years (Azure abused)
Registrar: MarkMonitor Inc.

URLScan.io + Hybrid Analysis Findings

26 HTTP transactions
6 domains contacted
6 IP connections across US + Cloudflare
Primary IP: 13.65.42.183 (Azure — San Antonio, US)

Additional IPs:
104.21.27.152 (Cloudflare)
104.17.25.14 (Cloudflare)
Final page: Fake banking login page

Technologies used: Bootstrap, jQuery, Modernizr, FontAwesome

No files extracted (pure credential phishing)

Indicators of Compromise (IOCs)
Domains
rbfcu-star.azurewebsites.net
(additional redirector domains from scan)

IP Addresses
13.65.42.183
104.21.27.152
104.17.25.14

Files
None (no payloads or malware dropped)

Threat Assessment

This is a high-severity credential harvesting campaign.
The attacker weaponizes trusted Azure infrastructure to bypass basic filtering and appear legitimate to victims.

Recommended Defensive Actions
1. Block identified IPs & domains
2. Add IOCs to SIEM (Splunk / Sentinel)
3. Enforce MFA for financial site access
4. Train users on banking login spoofing
5. Monitor for similar Azure-hosted phishing infrastructure
6. Skills Demonstrated
7. OSINT investigation
9. Network analysis
10. Sandbox usage
11. SOC-style IOC reporting
12. Threat classification
13. Web behavior analysis
