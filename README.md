# Medical Appointment No-Shows — Data Cleaning & Preprocessing

## Task Overview
This project is part of a Data Analyst Internship (Task 1).
The goal is to clean and preprocess a raw dataset using Python (Pandas) in Jupyter Notebook.

---

## Dataset
- **Name:** Medical Appointment No Shows
- **Source:** Kaggle — https://www.kaggle.com/datasets/joniarroba/noshowappointments
- **File:** KaggleV2-May-2016.csv
- **Original Size:** 110,527 rows × 14 columns

---

## Tools Used
- Python 3
- Pandas library
- Jupyter Notebook

---

## Problems Found in Raw Data

| Problem | Detail |
|---|---|
| Messy column names | Wrong spelling: Hipertension, Handcap. Hyphen in No-show. Mixed case. |
| Invalid age value | 1 row had Age = -1 (impossible) |
| Date format issue | Dates were in ISO format: 2016-04-29T18:38:08Z |
| Text in no_show column | Values were Yes/No instead of 1/0 |

---

## Cleaning Steps Done

1. Renamed all 14 columns to lowercase with underscores
   - Hipertension → hypertension
   - Handcap → handicap
   - No-show → no_show
   - PatientId → patient_id
   - AppointmentID → appointment_id
   - (and all remaining columns)

2. Removed 1 row where age = -1

3. Converted date columns from ISO datetime to DD-MM-YYYY format
   - ScheduledDay and AppointmentDay both cleaned

4. Mapped no_show column: Yes → 1, No → 0

5. Confirmed 0 missing values and 0 duplicate rows

---

## Final Dataset
- **File:** medical_appointments_cleaned.csv
- **Size:** 110,526 rows × 14 columns

---

## Files in This Repository

| File | Description |
|---|---|
| KaggleV2-May-2016.csv | Original raw dataset |
| medical_appointments_cleaned.csv | Final cleaned dataset |
| data_cleaning.ipynb | Jupyter Notebook with all cleaning code |
| README.md | This file — project summary |

---

## How to Run

1. Install Python and Jupyter Notebook
2. Install pandas: pip install pandas
3. Open data_cleaning.ipynb in Jupyter
4. Run all cells in order
5. Cleaned file will be saved automatically

---

## Author
Name: [AJAY K PAI]
Internship: Data Analyst Internship — Task 1
