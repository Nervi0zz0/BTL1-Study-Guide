# 📊 SIEM Analysis: Key Concepts

## What is a SIEM?

> A **SIEM (Security Information and Event Management)** is a technological solution that **aggregates, normalizes, and analyzes log data** generated by multiple sources within an organization's IT infrastructure (servers, firewalls, endpoints, applications, network devices, etc.).
>
> **Main Objective:** Provide **centralized visibility** over security events, enabling **early threat detection**, incident investigation, and **regulatory compliance** through the analysis and correlation of this data.

## ✨ Key Functions of a SIEM

A modern SIEM integrates several essential functions:

1.  **Log Aggregation:**
    * Collects logs from a wide variety of heterogeneous sources into a centralized repository. Common sources include: Windows Event Logs, Linux `syslog`, Firewall logs, Proxy, VPN, DNS, DHCP, Antivirus/EDR, web applications, databases, Cloud logs (`AWS CloudTrail`, `Azure Activity Log`, etc.).

2.  **Normalization:**
    * Logs come in many different formats. Normalization **parses** (analyzes and extracts) these logs and converts them into a **common, structured format**. This involves identifying and tagging key fields (timestamp, source IP, destination IP, user, action, etc.), which is fundamental for effectively searching and correlating data from different sources.

3.  **Correlation:**
    * It's the "brain" of the SIEM. It looks for **relationships and patterns** among events from different sources that, in isolation, might not seem suspicious, but together indicate a potential threat. It relies on predefined or custom **correlation rules** (e.g., "Multiple failed logins from one IP followed by a successful login" or "Communication from an internal server to a known C&C IP").

4.  **Alerting:**
    * When a correlation rule is met or a predefined critical event is detected, the SIEM generates an **alert** to notify the security team (SOC) for investigation.

5.  **Dashboards and Visualization:**
    * Presents security information graphically and summarized through **dashboards**, charts, and tables. Allows monitoring security status, viewing trends, active alerts, and key metrics at a glance.

6.  **Log Retention:**
    * Stores logs (raw and/or normalized) for a defined period. This is crucial for complying with regulations (e.g., `PCI DSS`, `GDPR`) and for enabling forensic investigations into past incidents.

7.  **Searching and Analysis (`Querying`):**
    * Offers a powerful query language (like `SPL` in `Splunk`, `KQL` in `Elastic`/`Sentinel`) that allows analysts to efficiently search terabytes of log data to investigate alerts, perform **threat hunting** (proactive threat searching), and generate custom reports.

## ✅ Why is a SIEM Important?

* **Centralized Visibility:** Breaks down log silos and offers a unified view.
* **Rapid Detection:** Reduces time to detect incidents through correlation and alerts.
* **Effective Incident Response:** Provides a central point to investigate what happened, when, and how.
* **Regulatory Compliance:** Helps meet audit and log retention requirements (`PCI DSS`, `HIPAA`, `GDPR`, etc.).
* **Threat Hunting:** Allows proactively searching for threats that haven't generated alerts.

## 🎯 BTL1 Focus

> In scenarios like BTL1, you will very likely encounter a SIEM interface (frequently **`Splunk`**) containing relevant logs for an incident. You will need to use the SIEM's search and filtering capabilities to find specific evidence, answer questions, and reconstruct attacker activity based on the available logs. You are expected to know how to build basic queries and filter large amounts of data to find pertinent information.

---

> _Understanding these key functions will help you comprehend what to expect from a SIEM and how to approach log analysis on platforms like `Splunk` or `Elastic Stack`._# 📊 SIEM Analysis: Key Concepts

## What is a SIEM?

> A **SIEM (Security Information and Event Management)** is a technological solution that **aggregates, normalizes, and analyzes log data** generated by multiple sources within an organization's IT infrastructure (servers, firewalls, endpoints, applications, network devices, etc.).
>
> **Main Objective:** Provide **centralized visibility** over security events, enabling **early threat detection**, incident investigation, and **regulatory compliance** through the analysis and correlation of this data.

## ✨ Key Functions of a SIEM

A modern SIEM integrates several essential functions:

1.  **Log Aggregation:**
    * Collects logs from a wide variety of heterogeneous sources into a centralized repository. Common sources include: Windows Event Logs, Linux `syslog`, Firewall logs, Proxy, VPN, DNS, DHCP, Antivirus/EDR, web applications, databases, Cloud logs (`AWS CloudTrail`, `Azure Activity Log`, etc.).

2.  **Normalization:**
    * Logs come in many different formats. Normalization **parses** (analyzes and extracts) these logs and converts them into a **common, structured format**. This involves identifying and tagging key fields (timestamp, source IP, destination IP, user, action, etc.), which is fundamental for effectively searching and correlating data from different sources.

3.  **Correlation:**
    * It's the "brain" of the SIEM. It looks for **relationships and patterns** among events from different sources that, in isolation, might not seem suspicious, but together indicate a potential threat. It relies on predefined or custom **correlation rules** (e.g., "Multiple failed logins from one IP followed by a successful login" or "Communication from an internal server to a known C&C IP").

4.  **Alerting:**
    * When a correlation rule is met or a predefined critical event is detected, the SIEM generates an **alert** to notify the security team (SOC) for investigation.

5.  **Dashboards and Visualization:**
    * Presents security information graphically and summarized through **dashboards**, charts, and tables. Allows monitoring security status, viewing trends, active alerts, and key metrics at a glance.

6.  **Log Retention:**
    * Stores logs (raw and/or normalized) for a defined period. This is crucial for complying with regulations (e.g., `PCI DSS`, `GDPR`) and for enabling forensic investigations into past incidents.

7.  **Searching and Analysis (`Querying`):**
    * Offers a powerful query language (like `SPL` in `Splunk`, `KQL` in `Elastic`/`Sentinel`) that allows analysts to efficiently search terabytes of log data to investigate alerts, perform **threat hunting** (proactive threat searching), and generate custom reports.

## ✅ Why is a SIEM Important?

* **Centralized Visibility:** Breaks down log silos and offers a unified view.
* **Rapid Detection:** Reduces time to detect incidents through correlation and alerts.
* **Effective Incident Response:** Provides a central point to investigate what happened, when, and how.
* **Regulatory Compliance:** Helps meet audit and log retention requirements (`PCI DSS`, `HIPAA`, `GDPR`, etc.).
* **Threat Hunting:** Allows proactively searching for threats that haven't generated alerts.

## 🎯 BTL1 Focus

> In scenarios like BTL1, you will very likely encounter a SIEM interface (frequently **`Splunk`**) containing relevant logs for an incident. You will need to use the SIEM's search and filtering capabilities to find specific evidence, answer questions, and reconstruct attacker activity based on the available logs. You are expected to know how to build basic queries and filter large amounts of data to find pertinent information.

---

> _Understanding these key functions will help you comprehend what to expect from a SIEM and how to approach log analysis on platforms like `Splunk` or `Elastic Stack`._