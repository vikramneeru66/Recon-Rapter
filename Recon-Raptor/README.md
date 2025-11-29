# 🦅 ReconRaptor

**ReconRaptor** is an automated information gathering toolkit built around the powerful Recon-ng framework. Designed for penetration testers and cybersecurity researchers, it simplifies domain reconnaissance by organizing tasks into automated workflows and storing results for analysis and reporting.

## 🔍 Project Goal

To provide a modular, efficient, and customizable way to perform open-source intelligence (OSINT) and domain reconnaissance using Recon-ng, all wrapped in a streamlined command-line and reporting workflow.

---

## 📦 Features

- 📁 Workspace-based project management
- 🌐 Domain and subdomain enumeration
- ⚙️ Integration with Recon-ng marketplace modules
- 📝 Auto-logging and reporting of gathered intelligence
- 🧠 Easy-to-read structure for expanding or customizing modules

---

## 🚀 Getting Started

### 📋 Prerequisites

- Python 3.8+
- Kali Linux (or any distro with Recon-ng installed)
- Internet connection (for API-based modules)

### 🔧 Installation

Clone this repository:

```bash
git clone https://github.com/your-username/ReconRaptor.git
cd ReconRaptor
Install required tools:


sudo apt update
sudo apt install recon-ng
(Optional) Create a Python virtual environment:


python3 -m venv venv
source venv/bin/activate
🛠️ Usage
1. Launch Recon-ng

recon-ng
2. Create Workspace

workspaces create vulnweb
3. Insert Domain

db insert domains domain=vulnweb.com notes="Testing Recon-ng" module=manual
If this gives a "Columns and values length mismatch" error, use manual insert via SQL or the correct insert syntax matching the schema.

4. Install & Use Modules
marketplace install recon/domains-hosts/hackertarget
modules load recon/domains-hosts/hackertarget
set SOURCE vulnweb.com
run
🧾 Project Structure

ReconRaptor/
├── recon/                # Scripts for launching Recon-ng
│   ├── start_recon.py
│   └── modules/          # Custom modules
├── workspaces/           # Output and database files
├── docs/                 # Guides and instructions
├── reports/              # Exported analysis reports
├── requirements.txt
└── README.md
📑 Example Output
After running modules, export and analyze data like subdomains, hosts, IPs, etc.

db query "SELECT * FROM hosts;"
