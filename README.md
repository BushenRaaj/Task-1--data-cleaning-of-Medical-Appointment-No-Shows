# Task 1 – Data Cleaning of Medical Appointment No Shows

This repository contains the solution for **Task 1: Data Analyst Internship Assignment**.  
The project focuses on cleaning and preprocessing the **Medical Appointment No Shows dataset (Kaggle, 2016)** to prepare it for further analysis.

## 📊 Dataset Information
- **File name:** Medical Appointment No Shows.csv  
- **Rows:** 110,527  
- **Columns:** 14  
- **Dataset description:** Contains information about patients’ medical appointments in Brazil and whether they showed up.  
- **Target column:** `No-show` (Yes = missed appointment, No = attended).  

### Key Columns:
- `PatientId` → Unique patient identifier  
- `AppointmentID` → Unique appointment identifier  
- `Gender` → Male/Female  
- `ScheduledDay` → Date/time appointment was scheduled  
- `AppointmentDay` → Date of appointment  
- `Age` → Patient age (0–115 years, one invalid record with -1)  
- `Neighbourhood` → Location of hospital/clinic  
- `Scholarship` → 1 if patient is enrolled in welfare program  
- `Hipertension`, `Diabetes`, `Alcoholism`, `Handcap` → Medical conditions  
- `SMS_received` → 1 if patient received an SMS reminder  
- `No-show` → Yes (missed) / No (attended)  

---

## 🧹 Cleaning Steps Performed
1. **Loaded dataset** into pandas.  
2. **Checked duplicates** → none found.  
3. **Fixed invalid ages** → one negative age replaced with median value.  
4. **Standardized categorical values**:
   - Gender: `M/F` → `Male/Female`  
5. **Parsed datetime columns**:
   - Converted `ScheduledDay` and `AppointmentDay` to proper datetime format.  
6. **Created new features**:
   - `wait_days` = number of days between scheduling and appointment.  
   - `no_show` = binary mapping of `No-show` column (`No=0`, `Yes=1`).  
7. **Renamed columns** to snake_case (e.g., `PatientId` → `patient_id`).  
8. **Exported cleaned dataset** to `Medical Appointment No Shows - Cleaned.csv`.  

---

## 📌 Summary

The **Medical Appointment No Shows** dataset contains over 110,000 medical appointment records from Brazil.  
The goal of this task was to clean and preprocess the raw data so it can be used for analysis and modeling.

### Key Cleaning Actions:
- Removed duplicate records.  
- Fixed invalid ages (e.g., negative age replaced with median).  
- Standardized categorical values (Gender → Male/Female).  
- Converted `ScheduledDay` and `AppointmentDay` into proper datetime format.  
- Engineered new feature: `wait_days` (days between scheduling and appointment).  
- Converted `No-show` into a binary column (`0 = attended`, `1 = missed`).  
- Renamed columns into a consistent snake_case format.  

### Deliverables:
- **Raw Dataset** → `Medical Appointment No Shows.csv`  
- **Cleaned Dataset** → `Medical Appointment No Shows- cleaned.csv`  
- **Jupyter Notebook** → `Task-1-Data-Cleaning-of-Medical-Appointment-No-Shows.ipynb`  

The cleaned dataset is now consistent, free of invalid values, and ready for **exploratory data analysis (EDA)** and **predictive modeling**.

---

## 📂 Repository Structure

- [Medical Appointment No Shows.csv](Medical%20Appointment%20No%20Shows.csv) → Raw dataset  
- [Medical Appointment No Shows- cleaned.csv](Medical%20Appointment%20No%20Shows-%20cleaned.csv) → Cleaned dataset  
- [Task-1-Data-Cleaning-of-Medical-Appointment-No-Shows.ipynb](Task-1-Data-Cleaning-of-Medical-Appointment-No-Shows.ipynb) → Jupyter Notebook (full workflow)  
- [README.md](README.md) → Documentation 
