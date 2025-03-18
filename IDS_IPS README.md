# IDS/IPS Configuration Documentation

## Overview
This section outlines the configuration and deployment of the Intrusion Detection and Prevention System (IDS/IPS) in the cyber lab setup. The tools being used are **Suricata** (for IDS) and **Snort** (for IPS), which are configured to detect and prevent network-based threats.

## Suricata IDS Setup
- **Location**: `IDS_IPS/suricata_config.yml`
- Suricata is configured to monitor incoming and outgoing network traffic, analyzing packet data for signs of malicious activity.
- Rules are configured to detect known attack patterns, including port scans, SQL injection attempts, and malware activity.
- **Log Location**: Logs are stored in `IDS_IPS/suricata_logs/`.

### Key Suricata Configurations:
- **Alert threshold**: Suricata is set to alert on high-severity events.
- **Logging**: Suricata writes logs in the JSON format, which are stored in the `logs/` folder.
- **Custom Rules**: Custom rules for specific attack vectors are stored in `suricata_rules/`.

## Snort IPS Setup
- **Location**: `IDS_IPS/snort_config.conf`
- Snort is configured as an intrusion prevention system that not only detects but also blocks malicious traffic based on predefined signatures.
- Snort is integrated with the firewall (iptables) to block malicious traffic in real time.
- **Rule Location**: `IDS_IPS/snort_rules/`.

### Key Snort Configurations:
- **Block rules**: Snort uses specific rule sets to block malicious traffic as soon as it’s detected.
- **Integration with iptables**: Snort’s alerts are used to trigger firewall rules that drop malicious packets.

## Integration with Other Tools
- **Suricata and Snort Integration**: Both Suricata and Snort are configured to provide real-time alerts and logs to be analyzed by the monitoring system.
- **Log Aggregation**: All IDS/IPS logs are aggregated in a centralized log server for analysis.
- **Firewall Interaction**: Both systems work in tandem with `iptables` to drop malicious packets and prevent further compromise.

## Future Improvements
- Integrating a centralized alerting system (e.g., ELK Stack) for better visualization and correlation of events.
- Automation scripts to dynamically update rules based on threat intelligence feeds.
