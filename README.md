MOHAMED MAMDOUH | Senior Document Controller & Data Analyst 🏗️📊
<p align="left">
<img src="https://img.shields.io/badge/Location-Dubai%2C%20UAE-blue?style=flat-square&logo=googlemaps" alt="Location">
<a href="mailto:mamduh.mohamed@yahoo.com"><img src="https://img.shields.io/badge/Email-mamduh.mohamed%40yahoo.com-red?style=flat-square&logo=gmail" alt="Email"></a>
<a href="https://www.linkedin.com/in/mohamed-mamdouh2020/"><img src="https://img.shields.io/badge/LinkedIn-Profile-blue?style=flat-square&logo=linkedin" alt="LinkedIn"></a>
<a href="https://www.coursera.org/user/b012bd8ee71c18a9a3364fb37417e079"><img src="https://img.shields.io/badge/Portfolio-Certificates-blueviolet?style=flat-square&logo=coursera" alt="Coursera Portfolio"></a>
</p>

🌟 Professional Overview
I help companies master large-scale project documentation by leveraging my engineering background and advanced data analytics skills. I build fast, audit-ready systems (Aconex + structured logs) that empower teams to retrieve any project information in seconds, significantly improving turnaround time and decision-making accuracy.

🚀 Key Professional Highlights
Efficiency: Improved document turnaround time from 7 days to 48 hours via workflow optimization.

Scale: Managing 80+ documents/day and repositories exceeding 11,000+ records.

Speed: Reduced average retrieval time from 3 minutes to 30 seconds.

Coordination: Managed approvals and distribution across 7+ key stakeholders (Client, Consultants, Contractors).

🛠️ Case Study 1: End-to-End Automation (1,000+ Requests)
Context: Consultant demanded submission of 1,000 requests within one week upon project commencement for 80 villas.
Solution: Developed a Python-based intelligent archiving pipeline to auto-split scanned documents based on page size.

<details>
<summary>📑 Show Python Code</summary>

Python
import fitz  # PyMuPDF
from PyPDF2 import PdfReader, PdfWriter

# Define A4 dimensions for detection
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
        for p in page_range: writer.add_page(reader.pages[p])
        with open(f"Request_{idx+1}.pdf", "wb") as f: writer.write(f)
</details>

Result: Transformed a 7-day manual workload into a 1-day automated process.

🔍 Case Study 2: Excel-based Local Document Search Engine
Context: Large repository of 11,000+ documents. Finding files quickly was impacting productivity.
Solution: Built a dynamic search tool using Advanced Excel Formulas (VSTACK, FILTER, SEARCH).

<details>
<summary>📑 Show Excel Formula</summary>

Excel
=FILTER(
    VSTACK(
        'IR-STR-LOG.xlsx'!Table2[#Data],
        'DS-LOG.xlsx'!Table4[#Data],
        'RFI-LOG.xlsx'!Table22[#Data]
    ),
    (ISNUMBER(SEARCH(A1, VSTACK('IR-STR-LOG.xlsx'!Table2[Description], ...)))) *
    (ISNUMBER(SEARCH(B1, VSTACK('RFI-LOG.xlsx'!Table22[Villa No.], ...)))),
    "No Match Found"
)
</details>

Result: Reduced retrieval time by 85%, cutting search time from 3 minutes to 30 seconds.

⚡ Case Study 3: The Technical Workflow (PowerShell & VBA)
Requirement: Creating 80 individual villa folders and corresponding Excel logs based on Consultant specifications.

1. PowerShell Script Generation (via Excel hyperlink logic)
<details>
<summary>📑 Show PowerShell Command Structure</summary>

PowerShell
# Command is dynamically generated within Excel for each row
Copy-Item -Path "Z:\Hyperlinked\Document.pdf" -Destination "D:\Consultant_Submission\Villa_110\"
</details>

2. VBA Data Segregation Macro (Master Log Splitting)
<details>
<summary>📑 Show VBA Macro</summary>

VBA
Sub SplitRequestsToSeparateFiles()
    Dim ws As Worksheet, dict As Object, i As Long, villaNo As Variant, lastRow As Long
    Set ws = ThisWorkbook.Sheets("IR&CPR")
    Set dict = CreateObject("Scripting.Dictionary")
    
    ' Loop to identify unique Villa Numbers
    lastRow = ws.Cells(ws.Rows.Count, 4).End(xlUp).Row
    For i = 2 To lastRow
        villaNo = ws.Cells(i, 4).Value
        If villaNo <> "" And Not dict.exists(villaNo) Then dict.Add villaNo, 1
    Next i
    
    ' Split and save separate workbooks
    For Each villaNo In dict.keys
        ws.UsedRange.AutoFilter Field:=4, Criteria1:=villaNo
        ws.UsedRange.SpecialCells(xlCellTypeVisible).Copy
        Workbooks.Add.Sheets(1).Paste
        ActiveWorkbook.SaveAs Filename:="D:\to_CONS\Villa_" & villaNo & ".xlsx"
        ActiveWorkbook.Close
        ws.AutoFilterMode = False
    Next villaNo
End Sub
</details>

📊 Technical Skills & Software Stack
EDMS: Oracle Aconex (Power User), SharePoint.

Automation: Python, VBA, PowerShell.

Data & Analysis: Microsoft Excel (Advanced), Power Query, Power BI.

Tools: Bulk PDF Filler, Bulk Rename Utility, Adobe Acrobat Pro.

💼 Professional Experience
Senior Document Control Specialist | Mass Group (New Administrative Capital) | Feb 2025 – Apr 2026

Client: Egyptian Presidency | Consultant: Designers Consultants & Associates

Document Control Specialist | S2A General Contracting (5th Settlement) | Sep 2024 – Feb 2025

Client: SKY AD. Developments | Consultant: ÖKOPLAN

Document Controller (Aconex) | MODAD (Wesal Fit Out Projects) | Sep 2022 – Aug 2024

Clients: Banque Misr, National Bank of Egypt (NBE)

🎓 Education & Certifications
B.Sc. Agricultural Science | Al-Azhar University.

Foundation in engineering fundamentals and industrial operational standards.

Aconex Accredited Professional | Oracle Certified (Mar 2024).

Google Data Analytics Professional Certificate (Jun 2022).

IELTS General Training | British Council (ID: 23EG504187AHMM001G).

❓ FAQ
Q: Are you available to work in Dubai/UAE?

A: Yes. Location: Dubai, UAE (As of April 2, 2026).

Q: What EDMS platforms do you specialize in?

A: Power User in Aconex (Workflows, Transmittals, Audit Trails) and SharePoint.

Q: Do you have experience with data analysis and automation?

A: Yes. Successfully replaced manual workflows with Python and VBA solutions, transforming weeks of work into hours.

<p align="center">
<b>Let's build something efficient together!</b>


<a href="https://www.linkedin.com/in/mohamed-mamdouh2020/">LinkedIn</a> |
<a href="mailto:mamduh.mohamed@yahoo.com">Email</a>
</p>
