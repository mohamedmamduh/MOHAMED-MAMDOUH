# MOHAMED MAMDOUH | Senior Document Controller & Data Analyst 🏗️📊

<p align="center">
  <img src="https://img.shields.io/badge/Location-Dubai%2C%20UAE-blue?style=for-the-badge&logo=googlemaps&logoColor=white" alt="Location">
  <a href="mailto:mamduh.mohamed@yahoo.com"><img src="https://img.shields.io/badge/Email-mamduh.mohamed%40yahoo.com-red?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
  <a href="https://www.linkedin.com/in/mohamed-mamdouh2020/"><img src="https://img.shields.io/badge/LinkedIn-Profile-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="https://www.coursera.org/user/b012bd8ee71c18a9a3364fb37417e079"><img src="https://img.shields.io/badge/Portfolio-Certificates-4C1D95?style=for-the-badge&logo=coursera&logoColor=white" alt="Coursera Portfolio"></a>
</p>

---

### 🌟 Professional Overview
> **Bridging the gap between Construction Document Control and Data Analytics.**
> I help companies master large-scale project documentation by leveraging my engineering background and advanced automation. I build fast, audit-ready systems (**Aconex + Python + VBA**) that empower teams to retrieve any project information in seconds.

---

### 📈 Performance Metrics
| ⚡ Efficiency | 📂 Scale | 🔍 Speed | 🤝 Coordination |
| :--- | :--- | :--- | :--- |
| **7 Days → 48 Hours** | **11,000+** Records | **3 Min → 30 Sec** | **7+ Stakeholders** |
| *Turnaround Time* | *Repository Size* | *Retrieval Speed* | *Distribution Matrix* |

---

### 🛠️ Strategic Case Studies

#### 1️⃣ Case Study: End-to-End Automation (1,000+ Requests)
**The Challenge:** Managing a logistical bottleneck of 1,000 requests for 80 villas within one week.
**The Solution:** Developed a Python-based intelligent archiving pipeline to auto-split scanned documents based on page dimensions.

<details>
<summary>📑 View Python Automation Code</summary>

  ```python
import fitz  # PyMuPDF
from PyPDF2 import PdfReader, PdfWriter
تعريف مقاس A4 بالبوينت
A4_WIDTH = 595
A4_HEIGHT = 842
TOLERANCE = 10
def is_a4(page):
width = page.rect.width
height = page.rect.height
return abs(width - A4_WIDTH) < TOLERANCE and abs(height - A4_HEIGHT) < TOLERANCE
def split_pdf_by_a4_starts(input_path):
doc = fitz.open(input_path)
split_ranges = []
current_range = []
for i, page in enumerate(doc):
    if is_a4(page):
        if current_range:
            split_ranges.append(current_range)
        current_range = [i]
    else:
        if current_range:
            current_range.append(i)

if current_range:
    split_ranges.append(current_range)

# استخدم PyPDF2 لكتابة الملفات
reader = PdfReader(input_path)

for idx, page_range in enumerate(split_ranges):
    writer = PdfWriter()
    for page_num in page_range:
        writer.add_page(reader.pages[page_num])
    output_path = f"output_part_{idx+1}.pdf"
    with open(output_path, "wb") as f:
        writer.write(f)
    print(f"✅ تم حفظ الملف: {output_path}")
    شغّل السكريبت على ملفك
    split_pdf_by_a4_starts("input.pdf")

  ```

</details>Result: 🚀 Transformed a 7-day manual workload into a 1-day automated process.2️⃣ Case Study: Dynamic Search Engine (11k+ Documents)The Challenge: Information fragmentation across multiple project logs impacting site productivity.The Solution: Built a dynamic retrieval tool using Advanced Excel Array Formulas.<details><summary>📑 View Excel Array Formula</summary>Excel=FILTER(

  ```
    VSTACK(
        'IR-STR-LOG.xlsx'!Table2[#Data],
        'DS-LOG.xlsx'!Table4[#Data],
        'RFI-LOG.xlsx'!Table22[#Data]
    ),
    (ISNUMBER(SEARCH(A1, VSTACK('IR-STR-LOG.xlsx'!Table2[Description], ...)))) *
    (ISNUMBER(SEARCH(B1, VSTACK('RFI-LOG.xlsx'!Table22[Villa No.], ...)))),
    "No Match Found"
    )
  ```
    
</details>Result: 🔍 85% improvement in retrieval speed for site engineers.💻 Technical Software StackEDMS: Oracle Aconex (Power User), SharePoint.Automation: Python (Pandas, PyMuPDF), VBA, PowerShell.Data Analysis: Microsoft Excel (Expert), Power Query, Power BI.Utilities: Bulk PDF Filler, Bulk Rename Utility, Adobe Acrobat Pro.💼 Professional ExperiencePeriodRoleCompany2025 - 2026Sr. Document Control SpecialistMass Group (New Administrative Capital)2024 - 2025Document Control SpecialistS2A General Contracting (5th Settlement)2022 - 2024Document Controller (Aconex)MODAD (Wesal Fit Out Projects)🎓 Education & CredentialsB.Sc. Agricultural Science | Al-Azhar University.Aconex Accredited Professional | Oracle Certified (2024).Google Data Analytics | Professional Certificate (2022).IELTS General Training | British Council.❓ Frequently Asked QuestionsAre you available to work in Dubai?Yes. I will be locally available in Dubai, UAE starting April 2, 2026.Do you specialize in automation?Absolutely. I replace manual "copy-paste" workflows with Python/VBA scripts to ensure 100% data integrity and speed.<p align="center"><b>Let's build something efficient together!</b><a href="https://www.linkedin.com/in/mohamed-mamdouh2020/"><img src="https://www.google.com/search?q=https://img.shields.io/badge/LinkedIn-Connect-blue%3Fstyle%3Dfor-the-badge%26logo%3Dlinkedin" alt="LinkedIn"></a><a href="mailto:mamduh.mohamed@yahoo.com"><img src="https://www.google.com/search?q=https://img.shields.io/badge/Email-Contact-red%3Fstyle%3Dfor-the-badge%26logo%3Dgmail" alt="Email"></a></p>
