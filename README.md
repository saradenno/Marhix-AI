🛡️ MarHix GRC Agent - Local AI-Powered Compliance Automation
A privacy-first, locally-deployable GRC (Governance, Risk & Compliance) agent for automated security posture assessment against NIS2, ISO 27001, and CIS Controls.
🎯 Project Overview
MarHix GRC Agent is a Windows-native compliance automation tool that continuously monitors and assesses organizational security posture against European cybersecurity frameworks. Unlike cloud-based solutions (OmniSec, Drata, Vanta), MarHix operates 100% locally with optional AI-powered insights, ensuring complete data sovereignty and GDPR compliance.
🔗 Built for: European SMEs, public institutions, healthcare organizations, and critical infrastructure operators requiring NIS2 compliance.
✨ Key Features

🏠 Local-First Architecture: Zero cloud dependency, complete tenant isolation
🇪🇺 EU Compliance Ready: Native NIS2 Directive 2022/2555 & ISO 27001:2022 mapping
🤖 AI-Powered Insights: Optional Falcon LLM integration for remediation guidance
⚡ Real-Time Monitoring: Continuous security posture assessment
📊 Executive Reporting: Clean HTML/PDF reports with risk visualization
🔧 Extensible Framework: YAML-based rule engine for custom compliance frameworks
🏗️ Architecture
MarHix GRC Agent
├── 📊 Data Collectors (PowerShell/Python)
│   ├── Microsoft Defender Status
│   ├── BitLocker Encryption
│   ├── Windows Firewall Rules
│   ├── User Account Management
│   ├── Group Policy Objects (GPO)
│   └── Security Event Logs
├── 🧠 Compliance Engine (Python)
│   ├── YAML Rule Engine
│   ├── NIS2/ISO 27001/CIS Mapping
│   ├── Risk Scoring Algorithm
│   └── CIS Benchmark Comparison
├── 🤖 AI Integration Layer
│   ├── Falcon LLM Summaries
│   ├── Remediation Recommendations
│   └── Executive Briefings
└── 📈 Reporting & Export
    ├── JSON/YAML Data Outputs
    ├── HTML Executive Reports
    ├── PDF Compliance Reports
    └── SaaS Integration Prep
🚀 Quick Start
powershell# 1. Clone repository
git clone https://github.com/marhix-ai/grc-agent.git
cd grc-agent

# 2. Install dependencies
pip install -r requirements.txt
Install-Module -Name Microsoft.PowerShell.Security, PSWindowsUpdate

# 3. Run initial assessment
.\collectors\Collect-DefenderStatus.ps1
python rule_engine.py defender-evidence-*.json --executive-summary

# 4. View results
start .\outputs\executive_summary_*.json

📋 Compliance Coverage
NIS2 Directive 2022/2555:

Article 21.2(a) - Protection against malware ✅
Article 21.2(e) - Data encryption at rest/transit ✅
Article 21.2(h) - Access control & asset management ✅
Article 23 - Incident reporting requirements 🚧

ISO 27001:2022:

A.9 - Access Control (9.1-9.4) ✅
A.10 - Cryptographic Controls ✅
A.12 - Systems Security (12.1-12.6) ✅
A.16 - Information Security Incident Management 🚧

CIS Controls v8:

Control 1 - Inventory and Control of Enterprise Assets ✅
Control 3 - Data Protection ✅
Control 5 - Account Management ✅
Control 10 - Malware Defenses ✅

🛠️ Technology Stack

Data Collection: PowerShell 5.1+, WMI, Windows APIs
Rule Engine: Python 3.8+, PyYAML, Jinja2
AI Integration: Falcon LLM (Hugging Face)
Reporting: WeasyPrint, ReportLab, HTML5/CSS3
Configuration: YAML-based rule definitions
Output Formats: JSON, YAML, HTML, PDF

🎓 Academic Project
This project is part of a 26-week internship program at MarHix AI (September 2025 - February 2026), focused on building European AI solutions with privacy-by-design principles.
