# 🔍 Information Gathering on a Target Website

This project demonstrates the use of basic reconnaissance tools to gather public information on a target domain. The goal is to identify potential security exposures using open-source tools.

---

## 🎯 Target

- Public Demo Target: `testphp.vulnweb.com` or `vulnweb.com`
- You can also use your local VM IP

---

## 🛠 Tools Used

- `whois` – for domain registration info
- `theHarvester` – for subdomains, emails, IPs
- `nmap` – for open ports, services, OS detection
- `recon-ng` – optional, advanced recon framework

---

## 🚀 Steps

1. **WHOIS Lookup**
   ```bash
   whois vulnweb.com > tools/whois_result.txt
   ```

2. **Run theHarvester**
   ```bash
   theHarvester -d vulnweb.com -b bing > tools/theharvester_result.txt
   ```

3. **Scan with Nmap**
   ```bash
   nmap -sV -A vulnweb.com > tools/nmap_scan.txt
   ```

4. *(Optional)* Recon-ng module execution
   - Configure workspace, add domain, run recon modules

---

## 📊 Sample Results

See results in the `/tools` directory and screenshots in `/screenshots`.

---

## ✅ Learning Outcome

- Understand the importance of passive & active recon
- Discover open ports, emails, subdomains, and potential threats

---

## 📁 Report

Detailed findings are documented in [`report/Information_Gathering_Report.md`](report/Information_Gathering_Report.md)

---

## 📷 Screenshots

Include screenshots of each tool’s output and any key findings.

---
