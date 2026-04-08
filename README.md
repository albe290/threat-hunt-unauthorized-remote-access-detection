🛡️ Threat Hunt Case Study: Unauthorized Remote Access Detection (Splunk + EDR)
📌 Overview

This project documents a threat intelligence-driven hunt focused on identifying unauthorized remote-access activity within an enterprise environment. The investigation was based on adversary tradecraft indicating the use of remote-access tools for potential hands-on-keyboard activity.

🎯 Objective

Identify and validate suspicious remote-access software execution outside approved enterprise controls, and determine whether activity represented benign usage, policy violation, or potential malicious behavior.

🛠️ Tools & Technologies
Splunk (log analysis & correlation)
Endpoint telemetry (EDR)
Threat Intelligence (adversary tradecraft)
Privileged Access Management telemetry
🔍 Methodology

1. Data Source Validation

Identified relevant index and sourcetype containing process execution telemetry
Validated schema and confirmed event structure

2. Discovery

Searched for remote-access software execution across telemetry
Confirmed presence of execution events

3. Scoping

Grouped activity by user and host
Identified frequency, first seen, and last seen activity

4. Deep Analysis

Reviewed raw event data and parsed nested fields
Analyzed execution paths, command-line arguments, and user context

5. Outlier Review

Investigated anomalies to distinguish benign activity from suspicious behavior

6. Stakeholder Validation

Partnered with infrastructure and software compliance teams
Validated whether observed software usage was approved or unauthorized
🚨 Key Findings
Identified unauthorized remote-access software execution across 6 users and multiple hosts
Observed execution from user-writable paths (Downloads, Desktop, Temp) instead of approved install locations
Detected repeated usage patterns indicating non-standard software behavior
Distinguished benign uninstall activity from potentially risky user-driven execution
Confirmed software was not approved and lacked enterprise licensing
⚙️ Detection Developed

Remote Access From User-Writable Path

Detects execution of remote-access tools outside approved install directories
Focuses on identifying control deviations rather than generic activity
Designed to reduce noise while improving detection visibility
📊 Outcome
No confirmed adversary compromise identified
Confirmed unauthorized software usage and policy/control gap
Detection created to improve monitoring
Recommendations provided for restriction and remediation
📈 Impact
Improved visibility into unauthorized remote-access activity
Enabled detection of control deviations in endpoint behavior
Strengthened monitoring and security operations response
🧠 Key Skills Demonstrated
Threat Hunting
Detection Engineering
Log Correlation (Splunk)
Endpoint Investigation
MITRE ATT&CK Alignment
Threat Intelligence Analysis
Security Reporting & Documentation
🔒 IMPORTANT NOTE

This project has been sanitized to remove all sensitive organizational details, including:

Usernames
Hostnames
Internal systems
Case identifiers

The focus is on demonstrating methodology, detection logic, and investigation workflow.
