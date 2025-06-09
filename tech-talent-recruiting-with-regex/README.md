# Tech Talent Recruiting with Regex 🧠💼

This project demonstrates how to extract key information from unstructured resume data using **Python**, **Pandas**, and **Regular Expressions (Regex)**. The aim is to assist a global HR consultancy in identifying tech talent quickly and accurately.

---

## 🧰 Tools & Technologies Used
- Python (Pandas, re)
- Jupyter Notebook
- CSV Parsing
- Regular Expressions (Regex)
- Data Cleaning and Preprocessing

---

## 🗂️ Dataset
- **Source:** Provided as `resumes.csv`
- **Columns:**
  - `ID` – Candidate unique identifier
  - `Resume_str` – Full resume content
  - `Category` – Resume domain

---

## 📊 Objective
1. Extract:
   - `job_title`: Most recent role
   - `tech_skills`: Technical skills (Python, SQL, R, Excel)
   - `education`: Highest educational degree
2. Clean and structure data into `candidates_df`
3. Ensure no nulls or empty strings
4. Prepare for downstream analytics or visualization

---

## 🔍 Key Code Logic

```python
def parse_resume(row):
    resume = row['Resume_str']
    job_title = ' '.join(resume.split()[:5])
    tech_skills = re.findall(r'\b(Python|SQL|R|Excel)\b', resume, re.IGNORECASE)
    education = re.search(r'\b(PhD|Master|Bachelor)\b', resume, re.IGNORECASE)
    ...

