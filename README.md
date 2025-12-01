## Career Atlas Salary Data Cleaning and Analysis

This project focuses on cleaning and analyzing a salary dataset provided by Career Atlas Inc. The goal is to correct inconsistencies, validate key fields, and uncover salary trends across experience levels, employment types, and remote work settings.

This practical exam demonstrates my ability to clean real-world datasets, apply validation rules, perform group-based salary analysis, and communicate findings clearly using Python and Jupyter Notebook.

---

## 1. Project Overview

Career Atlas Inc. noticed inconsistencies in reported salary data.  
The dataset contains job roles, experience levels, employment types, and salary values.  
My task was to clean the dataset and produce insights to support a reliable salary trend report.

Using Python and pandas, I:

- Cleaned invalid or missing values
- Validated categorical and numeric fields
- Imputed or replaced incorrect entries
- Removed unusable job titles
- Analyzed salary trends by experience and employment type
- Compared salaries between remote and on-site roles

---

## 2. Data Cleaning Rules Applied

The following cleaning and validation rules were used to produce the final `clean_salaries` DataFrame:

- **work_year:** must be an integer; missing values removed  
- **experience_level:** allowed values: EN, MI, SE, EX; invalid or missing set to EN  
- **employment_type:** allowed values: FT, PT, CT, FL; missing replaced with FT  
- **job_title:** entries with fewer than 3 characters removed  
- **salary_in_usd:** values below 10,000 or above 1,000,000 replaced with median  
- **company_location:** must be a 2-letter country code; missing replaced with US  
- **company_size:** must be S, M, or L; invalid/missing replaced with M  

---

## 3. Salary Trends by Experience Level

Using the cleaned data, I grouped by:

- `experience_level`
- `employment_type`

and calculated the average salary.

The resulting DataFrame is saved as `salary_trends`.

### Key Findings

- Senior (SE) and Executive (EX) roles consistently earn the highest salaries across all job types.
- Full-time (FT) employees showed the largest spread in salary differences between experience levels.
- Entry-level (EN) roles have the lowest average salary, as expected.

---

## 4. Remote Work Salary Comparison

To understand the impact of remote work:

- Remote roles: `remote_ratio = 100`
- On-site roles: `remote_ratio = 0`

The comparison was saved as `remote_salary_comparison`.

### Observations

- Remote roles generally have **higher average salaries**, suggesting companies may pay more to attract distributed talent.
- On-site roles had more variation but lower overall averages.

---

## 5. Tools and Libraries Used

- Python  
- pandas  
- NumPy  
- Jupyter Notebook  

---

## 6. What This Project Demonstrates

- Ability to clean and validate real-world messy data  
- Understanding of categorical and numeric correction techniques  
- Skill in grouping, aggregating, and interpreting salary trends  
- Experience presenting insights clearly using markdown  
- Reproducible analysis using Jupyter Notebook  

