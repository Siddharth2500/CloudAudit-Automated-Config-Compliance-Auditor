# 🚀 CloudAudit — Automated Configuration & Compliance Auditor

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg?logo=python&logoColor=white)  
![Tool](https://img.shields.io/badge/Compliance-Auditor-FF5252.svg?logo=shield)  
![Features](https://img.shields.io/badge/Features-Config-Checks-4CAF50.svg?logo=gear)  
![Reports](https://img.shields.io/badge/Reports-JSON-2196F3.svg?logo=json)  
![CI/CD](https://img.shields.io/badge/CI/CD-Ready-2088FF.svg?logo=githubactions)  
![Dependencies](https://img.shields.io/badge/Dependencies-None-green.svg?logo=python)

**CloudAudit** is a **Python 3** tool designed to scan cloud-resource configurations and evaluate them against predefined rules covering encryption, TLS version, and public access. It’s built for cloud engineers, DevOps, and compliance teams, offering a lightweight, extensible, and easily-integrated solution for auditing infrastructure settings.

------

## 🛠 Tech & Languages

| Layer        | Tech / Format                | Purpose                                 |
|--------------|------------------------------|-----------------------------------------|
| Language     | **Python 3.10+**             | Main codebase                           |
| Core Logic   | JSON parsing + Rule Engine   | Evaluate resource configurations        |
| Reports      | **JSON**                     | Summary output of audit results         |
| Execution    | Script / Colab / Notebook    | Supports quick analysis and prototyping |
| Logging      | Console + File Output        | Audit trail and human feedback          |

---

## 🌐 Architecture

Flow:  
1. **Load** configuration JSON file containing cloud resources (e.g., storage buckets, compute VMs, databases)  
2. **Evaluate** each resource:  
   - Check if encryption is enabled  
   - Verify TLS version meets minimum  
   - Confirm public access is disabled if required  
3. **Aggregate** results: count compliant vs non-compliant resources; collect a list of failures  
4. **Generate** `audit_report.json` with summary and detailed issues; print a human-readable summary  
5. **Integrate** the report into CI/CD pipelines, dashboards, or compliance workflows  

---

## ▶️ Run CloudAudit

```bash
python cloudaudit.py --input data/configurations.json --output data/audit_report.json
