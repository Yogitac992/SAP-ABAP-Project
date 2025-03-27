# SAP-ABAP-Project
z_material-report

# Z_MATERIAL_REPORT 🚀

## 📌 Project Overview  
This is a **Basic ABAP Report** that fetches **Material Master Data** from the MARA table.  
The report retrieves the **first 10 materials** and displays their **Material Number, Type, and Industry Sector**.

## ⚡ Features  
✔️ Fetches Material Data from MARA table  
✔️ **SELECT Query** with performance optimization (`UP TO 10 ROWS`)  
✔️ **Simple LOOP & WRITE statements** for output  

## 📜 ABAP Code 

REPORT ZMATERIAL_REPORT.

TABLES: MARA.

DATA: lt_mara TYPE TABLE OF MARA.

SELECT * FROM MARA INTO TABLE lt_mara UP TO 10 ROWS.

LOOP AT lt_mara INTO DATA(ls_mara).
  WRITE: / ls_mara-MATNR, ls_mara-MTART, ls_mara-MBRSH.
ENDLOOP.
