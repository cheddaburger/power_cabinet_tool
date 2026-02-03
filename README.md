# Power Cabinet Battery Monitor

A lightweight CLI tool to collect **battery state-of-charge (%)** and **backup runtime (minutes)** from power cabinet web interfaces during outage and disaster recovery events.

Designed for fast triage when dozens (or hundreds) of sites are impacted.

---

## Features

- Vendor-agnostic power cabinet web UI scraping  
- Secure credential handling via environment variables (`.env`)  
- Supports CSV or XLSX input  
- Automatic output timestamping (Excel-lock safe)  
- Sorts results by lowest battery first  
- Clean CLI interface  
- Debug artifacts saved automatically when parsing fails  

---

## Quick Start

### 1. Create and activate a virtual environment (Windows)

Run:  
`python -m venv venv`  
`venv\Scripts\activate`

---

### 2. Install dependencies

Run:  
`pip install -r requirements.txt`

---

### 3. Initialize credentials

Run:  
`python power_cabinet_tool.py --init-env`

---

### 4. Update `.env`

Edit the generated `.env` file and set:

`CABINET_USER=Admin`  
`CABINET_PASS_1=your_password_here`  
`CABINET_PASS_2=your_backup_password`

---

### 5. Run the tool

Run:  
`python power_cabinet_tool.py sites.xlsx`
