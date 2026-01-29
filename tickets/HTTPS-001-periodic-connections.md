# SOC Ticket: Possible Beaconing Activity via Periodic HTTPS Connections

## Scenario Context
- Alert generated from network monitoring system
- Internal employee workstation observed communicating with external domain
- Attempts are made at exact 60-seconds intervals
- HTTPS protocol used for communication
- Destination domain newly registered with no established reputation
- Traffic observed outside normal business hours

## Alert Summary
An alert was triggered due to repeated HTTPS connection attempts from an internal host to an external domain with unknown reputation. The connections were observed at fixed 60-second intervals outside normal business hours.

## Environment
The activity originated from an internal employee workstation within the corporate network. The traffic was observed outside standard working hours.

## Evidence Collected
- Source IP identified as an internal employee workstation
- HTTPS connections made to a newly registered domain with unknown reputation
- Network traffic observed at exact 60-second intervals
- Successful TLS handshakes observed for each connection

## Analyst Assessment
The traffic pattern is suspicious due to its precise and consistent timing, which is commonly associated with automated processes rather than normal human behavior. The use of HTTPS may indicate an attempt to conceal command-and-control communication. Additionally, the destination domain’s unknown reputation further increases the risk of malicious activity.

## Verdict
Suspicious – Monitoring

## Recommended Action
- Continue monitoring the host for persistent or evolving periodic connections
- Perform domain enrichment using WHOIS and passive DNS analysis
- Review endpoint telemetry for additional indicators of compromise
- Escalate to Tier 2 SOC for further investigation if the behavior persists or evolves
