# MITRE ATT&CK Mapping

Techniques observed in honeypot data or covered by my detections.

| Observation / Detection | Data source | Tactic | Technique |
| --- | --- | --- | --- |
| Password guessing (weak + botnet passwords) | Cowrie, Grafana alert, Suricata SID 1000002 | Credential Access | T1110.001 Brute Force: Password Guessing |
| Default account attempts (ubuntu, psql, root) | Cowrie | Initial Access | T1078.001 Valid Accounts: Default Accounts |
| Attacker SSH key planted in authorized_keys | Cowrie | Persistence | T1098.004 Account Manipulation: SSH Authorized Keys |
| chattr -ia .ssh to unlock protected files | Cowrie | Defense Evasion | T1222.002 File and Directory Permissions Modification: Linux |
| uname -a and system recon | Cowrie | Discovery | T1082 System Information Discovery |
| File download via wget/curl | Cowrie, Grafana alert | Command and Control | T1105 Ingress Tool Transfer |
| DNS lookup of watchlisted domain | Suricata SID 1000001, Grafana alert | Command and Control | T1071.004 Application Layer Protocol: DNS |
