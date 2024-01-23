# Blueprint-Incident-Response

## 72 Hours of Incident Response 💻🕒🔐

### Setting the Stage
Financial Institute
Tipped By: • Private sector (multiple times) • Law enforcement
Business continuity is critical • Critical production environment
IT personnel not security aware

###
Friday 18:15
CERT Hotline Call
~23:00 - EDR installed on critical systems, time for bed!
```
Custom: Hey, we need help
L1: We're here to help!
Custom: We were notified by law enforcement, apparently we're breached?
L1: By whom?
Custom: Law enforcement... We think?
L1: This sounds serious
```
###
Saturday 
09:30
Exfiltration observed
###
Saturday 10:30
Summary presentation
 EDR alert observed
• Rclone masqueraded as “veeam.exe”
• Final step before ransomware execution
• A decision must be made
```
L2: Hey do you use rclone?
Custom: rclone?
L2: We need to meet, ASAP
Custom: :(
```
###
Do You Pull the Plug?
Stay ONLINE - Risk ransomware encryption
<->
Go OFFLINE - Business continuity in jeopardy
###
Saturday 14:00
Okay we’re offline, now what?
Discussing investigation approach
 
 Analyze the received data
• Focus on initial foothold
• Determine scope of compromise
 
 Build a timeline
 2 tracks: Investigation / Operational
###
Saturday 19:00
Investigation update
Initial timeline
• First signs of compromise: 1 month earlier
 Discuss how to get back online (safely!)
 EDR needs to be installed on all systems
###
Sunday 00:00
End of day update
Additional findings
• First signs of compromise: 2 months earlier
 Threat Actor activities:
• Looking for KeePass data
• RDP and AnyDesk
• Netscan (Portscanner)
• PowerView
• RClone
 Logs show suspicious SonicWall VPN connections
###
Sunday 10:00
Operational update
Assemble on-site team
• RM&G (Risk Management & Governance)
• Pentester
 Focus on containment and mitigation
 Pentester needed to identify:
• Vulnerabilities
• Misconfigurations
```
target-query -f evtx /path/to/images/ | rdump -w splunk://10.31.3.37:6969
```
-> Filtered services overview (Dashboard)
###
Sunday 14:00
Investigation update
Follow the evidence
• Link to TA found (not communicated yet)
• How did they access the VPN?
• Other machines compromised?
 
 Attacker stats:
• 4 known compromised machines
• 3 known compromised users
 68 systems analyzed, 75 in EDR
###
Sunday 23:00
End of day update
Containment and mitigation
 Investigation continues
 Investigate actor TTPs:
• SonicWall exploitation (CVE-2019-7481)
• Usage of:
– Netscan
– RClone
– SOMBRAT (semi-custom malware)
###
Monday 14:00
Investigation update
Threat actor link communicated
• 2 infected devices (1 Domain Controller)
 Focus on SonicWall VPN
 Attacker stats:
• 5 known compromised machines
• 6 known compromised users
 93 systems analyzed, 111 in EDR
###
Monday 14:00
Operational update
Reconnecting to the internet (slowly!)
• EDR install is a prerequisite
 Call in all users to reset their passwords
 Kerberos reset
```
“Oh btw… we ehh, got stuff to 
do tonight, talk tomorrow?”
```
###
Tuesday 18:00
End of day update
Initial infection vector confirmed
• SonicWall exploited (CVE-2019-7481)
 Timeline expanded
• First signs of compromise: 8 (!) months earlier
 Attacker stats:
• 7 known compromised machines
• 8 known compromised users
 115 systems analyzed, 135 in EDR
###
After 72 hours
Aftercare
Fox-IT 24/7 EDR monitoring
 Continuation of:
• Investigation / pentest
• Assistance rebuilding / hardening environment
 Set up network monitoring
 Get environment online
 
 239 systems analyzed, 264 in EDR
###
Timeline
```
Q1 2021
Attacker activity
First activity originating 
from SonicWall

Q2 2021
Attacker returns
Scan executed, 
authentication attempts

Q3 2021
Password spray for 
multiple accounts

Q3 2021
SOMBRAT
Backdoor installed
SonicWall patched in this period

Q3 2021
AnyDesk activity
Remote Management 
Tooling favored by TA

Q3 2021
Data exfiltration
RClone usage observed

Q3 2021
Fox-IT involve
```
