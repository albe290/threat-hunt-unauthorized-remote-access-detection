# 🛡️ Threat Hunt Case Study: Unauthorized Remote Access Detection (Splunk + EDR)

## 📌 Overview

This project documents a **threat intelligence-driven hunt** focused on identifying unauthorized remote-access activity within an enterprise environment. The investigation was initiated based on adversary tradecraft indicating the use of remote-access tools for potential hands-on-keyboard activity.

The goal of this hunt was to determine whether observed activity represented **benign usage, policy violation, or potential malicious behavior**, while improving detection visibility and operational awareness.

---

## 🎯 Objective

* Identify suspicious remote-access software execution
* Validate whether activity aligns with approved enterprise controls
* Distinguish benign vs non-standard vs potentially malicious behavior
* Develop detection logic to improve visibility into control gaps

---

## 🛠️ Tools & Technologies

* **Splunk** – log analysis and correlation
* **Endpoint Detection & Response (EDR)** – endpoint telemetry analysis
* **Threat Intelligence** – adversary tradecraft and behavioral context
* **Privileged Access Management Telemetry** – process execution visibility

---

## 🔍 Methodology

### 1. Data Source Validation

* Identified relevant telemetry sources and validated event structure
* Confirmed process execution logs and required fields were present

### 2. Discovery

* Searched for remote-access software execution across telemetry
* Confirmed presence of relevant execution events

### 3. Scoping

* Grouped activity by user and host
* Identified frequency, first seen, and last seen activity

### 4. Deep Analysis

* Reviewed raw event data and parsed nested fields
* Analyzed execution paths and command-line arguments
* Validated user context and process behavior

### 5. Outlier Review

* Investigated anomalies to separate benign activity from suspicious behavior

### 6. Stakeholder Validation

* Partnered with infrastructure and software compliance teams
* Validated whether observed software usage was approved or unauthorized

---

## 🚨 Key Findings

* Identified unauthorized remote-access software execution across **6 users and multiple hosts**
* Observed execution from **user-writable paths** (e.g., Downloads, Desktop, Temp)
* Detected repeated execution patterns indicating non-standard behavior
* Distinguished benign uninstall activity from higher-risk execution patterns
* Confirmed software was **not approved** and lacked enterprise licensing

---

## ⚙️ Detection Use Case

### Remote Access Tool Execution from User-Writable Paths

**Description:**
Detects execution of remote-access tools outside approved installation directories.

**Detection Logic Focus:**

* Execution from user-writable paths
* Non-standard install locations
* Repeated execution patterns

**Outcome:**

* Improved visibility into unauthorized software usage
* Reduced detection noise by focusing on high-signal behavior

---

## 📊 Metrics

* **Hunt window:** 30 days
* **Users identified:** 6
* **Hosts analyzed:** multiple
* **Detection created:** 1
* **Outcome:** confirmed policy/control gap

---

## 📈 Outcome

* No confirmed adversary compromise identified
* Confirmed **unauthorized software usage**
* Identified **policy/control gap**
* Detection created to improve monitoring
* Recommendations provided for restriction and remediation

---

## 🧠 Analyst Notes

* Focused on **behavioral detection**, not just tool presence
* Prioritized **control deviation detection** over generic alerts
* Maintained analytical discipline by **not over-attributing** activity without sufficient evidence
* Demonstrated the importance of **stakeholder validation in threat hunting workflows**

---

## 🧩 Key Skills Demonstrated

* Threat Hunting
* Detection Engineering
* Log Correlation (Splunk)
* Endpoint Investigation
* MITRE ATT&CK Alignment
* Threat Intelligence Analysis
* Security Reporting & Documentation

---

## 📂 Repository Structure

```bash
threat-hunt-unauthorized-remote-access-detection/
│
├── README.md
├── queries/
├── screenshots/
├── report/
```

---

## 🔒 Disclaimer

This project has been **sanitized** to remove all sensitive organizational details, including:

* Usernames
* Hostnames
* Internal systems
* Case identifiers

The purpose of this repository is to demonstrate **threat hunting methodology, detection development, and investigation workflow** in a safe and professional manner.

---



