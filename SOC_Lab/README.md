# SOC Arquitecture & Infrastructure:

## NIST CSF Domains & Relevant Kali Purple Tools:



Here's a mapping of the NIST CSF Identify, Protect, Detect, Respond, Recover domains to tool categories and example tools available in Kali Purple (this is not exhaustive, and tools often span multiple domains):

<div align="center">
<img src="sources/networksqueme1.png" alt="Network topology" width="600"/>
</div>

    IDENTIFY (ID): Develop an organizational understanding to manage cybersecurity risk to systems, assets, data, and capabilities.
        Asset Management (ID.AM):
            Tools for asset discovery: nmap, rustscan, masscan, amap (in Kali - network mappers, service detection)
            Network documentation/mapping tools: zenmap (Nmap GUI), automapper (Kali - network topology mapping)
        Vulnerability Management (ID.VM):
            Vulnerability scanners: nessus, openvas (Greenbone Vulnerability Manager - pre-installed in some Kali versions), nikto (web vuln scanner), wpscan (WordPress scanner), nmap scripts for vulnerability detection.
            Vulnerability data management (less direct tools in Kali, but output can be used): Consider integrating with dedicated vulnerability management platforms outside of Kali for a full workflow in a real SOC. Kali focuses more on the scanning part.
        Risk Assessment (ID.RA):
            Frameworks & methodologies (conceptual, less tool-driven in Kali): Understanding of frameworks like NIST CSF itself, MITRE ATT&amp;CK.
            Configuration assessment/security auditing tools: lynis (security auditing and hardening recommendations - can inform risk), cve-search (Kali - CVE database search, useful in risk context).
        Threat Intelligence (ID.TI):
            Threat intelligence feeds/platforms (Kali doesn't directly host feeds, but can consume them): Integrate with external threat intelligence sources (e.g., MISP - Malware Information Sharing Platform, often used in SOCs, can be set up separately and integrated).
            OSINT (Open Source Intelligence) tools in Kali: theharvester, metagoofil, recon-ng, spiderfoot (information gathering from public sources).

    PROTECT (PR): Develop and implement appropriate safeguards to ensure delivery of critical infrastructure services.
        Identity Management and Access Control (PR.AC):
            Password auditing/cracking tools (for testing strength, not direct protection tools): john, hashcat (password crackers - used to test password policies and strength).
            Authentication testing tools (again, for testing, can inform protection): hydra, medusa (brute-force login testers).
        Awareness and Training (PR.AT): Less tool-driven, more about processes and education. Kali is used for demonstrating vulnerabilities to raise awareness.
        Data Security (PR.DS):
            Encryption tools (not SOC-specific, but fundamental): gpg, openssl (encryption/decryption utilities in Kali).
        Information Protection Processes and Procedures (PR.IP): Again, more process-driven, less direct tools in Kali. Relates to policies, procedures for data handling.
        Protective Technology (PR.PT):
            Firewall testing/configuration tools: nmap (firewall rule testing), iptables, nftables (command-line firewall management - can be used on target VMs to set up firewalls, and Kali to test).
            Intrusion Prevention Systems (IPS) testing: Kali Purple includes Suricata and Zeek (IDS/NSM - can be used in detection, but rulesets can be configured for prevention in some scenarios - less direct IPS role in default Kali Purple setup, more detection focus).
            Endpoint Security Testing (Evasion, Antivirus testing): Tools for testing antivirus evasion (Metasploit framework, custom payloads, though ethical use is crucial).

    DETECT (DE): Develop and implement appropriate activities to identify the occurrence of a cybersecurity event.
        Anomalies and Events Detection (DE.AE):
            Intrusion Detection Systems (IDS): Suricata, Zeek (pre-installed in Kali Purple - for network intrusion detection and network security monitoring).
            Log analysis tools: grep, awk, sed, scripting (Bash, Python) for parsing and analyzing logs (can be applied to logs collected from target VMs). ELK/Graylog (for more advanced log management, needs separate setup).
        Security Continuous Monitoring (DE.CM):
            Network monitoring tools: wireshark, tcpdump, tshark (packet capture and analysis). ntopng (network traffic monitoring).
            *System monitoring (less directly within Kali Purple's pre-installed tools, but can use standard Linux monitoring tools if needed, or integrate with external monitoring systems).
        Detection Processes (DE.DP): More about defining procedures and workflows for incident detection and alerting, less specific tools within Kali Purple itself for defining these procedures.

    RESPOND (RS): Develop and implement appropriate activities to take action regarding a detected cybersecurity incident.
        Response Planning (RS.RP): Process and procedure definition, less tool-specific in Kali Purple.   

    Analysis (RS.AN):
        Forensics tools: Autopsy (digital forensics platform - pre-installed in Kali Purple), bulk_extractor, strings, binwalk (forensic data extraction and analysis), Volatility (memory forensics - install separately if needed).
        Malware analysis tools (some basic tools in Kali, more advanced analysis often requires separate VMs/sandboxes): radare2 (reverse engineering framework), strings, ltrace, strace.
        Network forensics tools (Wireshark, tshark for deeper packet analysis).
    Mitigation (RS.MI):
        Tools for containment/isolation (less direct tools in Kali Purple for active mitigation of running systems, more focus on identifying mitigation steps based on analysis): Kali is more of an analysis platform than an active response platform in a live network. Mitigation often involves actions on other systems (firewalls, endpoint protection, etc.). Kali can be used to test mitigation effectiveness.
        Scripting for automation of simple response actions (e.g., firewall rule updates, but this requires integration with other systems and is advanced).
    Improvements (RS.IM): Process of post-incident review and improvement, less tool-driven.

RECOVER (RC): Develop and implement appropriate activities to maintain plans for resilience and to restore capabilities or services that were impaired due to a cybersecurity incident.

    Recovery Planning (RC.RP): Process and procedure definition.
    Improvements (RC.IM): Post-recovery improvements and lessons learned, process-focused.
    Communications (RC.CO): Communication plans during and after recovery.
