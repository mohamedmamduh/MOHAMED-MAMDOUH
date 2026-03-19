Markdown
# MOHAMED MAMDOUH | Senior Document Controller & Data Analyst 🏗️📊

<p align="center">
  <img src="[https://img.shields.io/badge/Location-Dubai%2C%20UAE-blue?style=for-the-badge&logo=googlemaps&logoColor=white](https://img.shields.io/badge/Location-Dubai%2C%20UAE-blue?style=for-the-badge&logo=googlemaps&logoColor=white)" alt="Location">
  <a href="mailto:mamduh.mohamed@yahoo.com"><img src="[https://img.shields.io/badge/Email-mamduh.mohamed%40yahoo.com-red?style=for-the-badge&logo=gmail&logoColor=white](https://img.shields.io/badge/Email-mamduh.mohamed%40yahoo.com-red?style=for-the-badge&logo=gmail&logoColor=white)" alt="Email"></a>
  <a href="[https://www.linkedin.com/in/mohamed-mamdouh2020/](https://www.linkedin.com/in/mohamed-mamdouh2020/)"><img src="[https://img.shields.io/badge/LinkedIn-Profile-0077B5?style=for-the-badge&logo=linkedin&logoColor=white](https://img.shields.io/badge/LinkedIn-Profile-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)" alt="LinkedIn"></a>
  <a href="[https://www.coursera.org/user/b012bd8ee71c18a9a3364fb37417e079](https://www.coursera.org/user/b012bd8ee71c18a9a3364fb37417e079)"><img src="[https://img.shields.io/badge/Portfolio-Certificates-4C1D95?style=for-the-badge&logo=coursera&logoColor=white](https://img.shields.io/badge/Portfolio-Certificates-4C1D95?style=for-the-badge&logo=coursera&logoColor=white)" alt="Coursera Portfolio"></a>
</p>

---

### 🌟 Professional Overview
> **"Engineering Precision Meets Data Automation."**
> I help construction firms manage massive documentation lifecycles by building audit-ready systems. Expert in **Oracle Aconex** and **Python automation**, focused on converting manual bottlenecks into high-speed digital workflows.

---

### 📊 Performance Dashboard
| ⚡ Efficiency | 📂 Scale | 🔍 Search Speed | 🤝 Coordination |
| :--- | :--- | :--- | :--- |
| **7 Days → 48 Hours** | **11,000+** Documents | **3 Min → 30 Sec** | **7+ Stakeholders** |
| *Workflow Optimization* | *Project Repository* | *Retrieval Metric* | *Matrix Management* |

---

### 🛠️ Strategic Case Studies

#### 1️⃣ Case Study: End-to-End Automation (1,000+ Requests)
**The Challenge:** Processing 1,000 requests for 80 villas in one week.
**The Solution:** Built a Python-based intelligent pipeline to auto-split scanned documents by page dimensions.

<details>
<summary>📑 View Python Splitter Logic</summary>

```python
import fitz  # PyMuPDF
from PyPDF2 import PdfReader, PdfWriter

# Define A4 dimensions (Points)
A4_WIDTH, A4_HEIGHT = 595, 842
TOLERANCE = 10

def is_a4(page):
    width, height = page.rect.width, page.rect.height
    return abs(width - A4_WIDTH) < TOLERANCE and abs(height - A4_HEIGHT) < TOLERANCE

def split_pdf_by_a4_starts(input_path):
    doc = fitz.open(input_path)
    split_ranges, current_range = [], []
    
    for i, page in enumerate(doc):
        if is_a4(page):
            if current_range: split_ranges.append(current_range)
            current_range = [i]
        else:
            if current_range: current_range.append(i)
            
    if current_range: split_ranges.append(current_range)
    
    reader = PdfReader(input_path)
    for idx, page_range in enumerate(split_ranges):
        writer = PdfWriter()
        for p in page_range:
            writer.add_page(reader.pages[p])
        with open(f"Request_{idx+1}.pdf", "wb") as f:
            writer.write(f)
```
</details>

2️⃣ Case Study: Advanced Search Engine (11k+ Logs)
The Challenge: Fragmented data across multiple stakeholder logs.
The Solution: Dynamic indexing via Excel Array Formulas.

<details>
<summary>📑 View Search Engine Formula</summary>

Excel
=FILTER(
    VSTACK('Log1.xlsx'!Table2[#Data], 'Log2.xlsx'!Table8[#Data]),
    (ISNUMBER(SEARCH(A1, VSTACK('Log1.xlsx'!Table2[Description], ...)))) *
    (ISNUMBER(SEARCH(B1, VSTACK('Log1.xlsx'!Table2[Villa No.], ...)))),
    "No Match Found"
)
</details>

3️⃣ Case Study: Technical Workflow (PowerShell & VBA)
The Challenge: High-precision data segregation for 80 individual villa folders.

<details>
<summary>📑 View PowerShell & VBA Logic</summary>

PowerShell
# PowerShell: Automated File Migration
Copy-Item -Path "Source_Link" -Destination "D:\to_CONS\Villa_110\"
VBA
' VBA: Master Log Segregation Macro
Sub SplitRequestsToFiles()
    ' ... Logic to split Master Log into 80 Workbooks
    ActiveWorkbook.SaveAs Filename:="D:\to_CONS\Villa_" & villaNo & ".xlsx"
End Sub
</details>

💻 Technical Software Stack
EDMS: Oracle Aconex (Accredited Professional), SharePoint.

Automation: Python (PyMuPDF), VBA, PowerShell.

Analysis: Advanced Excel (Power Query), Power BI.

Compliance: Naming Conventions, Revision Control, Audit Readiness.

💼 Professional Experience
Sr. Document Control Specialist | Mass Group (New Capital) | 2025 – 2026

Document Control Specialist | S2A General Contracting | 2024 – 2025

Document Controller (Aconex) | MODAD | 2022 – 2024

🎓 Education & Credentials
B.Sc. Agricultural Science | Al-Azhar University.

Aconex Accredited Professional | Oracle.

Google Data Analytics Professional Certificate.

IELTS General Training | British Council.

❓ FAQ
Are you available to work in Dubai?
Yes. I will be locally available in Dubai, UAE starting April 2, 2026.

<p align="center">
<a href="https://www.linkedin.com/in/mohamed-mamdouh2020/">
<img src="https://img.shields.io/badge/LinkedIn-Connect-blue?style=for-the-badge&logo=linkedin" alt="LinkedIn">
</a>
</p>
