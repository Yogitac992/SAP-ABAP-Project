# 🚀 SAP ABAP Project - Z_MATERIAL_REPORT

## 📌 Project Overview  
This is a basic ABAP report that retrieves Material Master Data from the MARA table.  
It fetches the first 10 materials and displays their Material Number (MATNR), Material Type (MTART), and Industry Sector (MBRSH)**.

---

## ⚡ Features  
✔️ Fetches Material Data from SAP MARA Table  
✔️ Uses SELECT Query with `UP TO 10 ROWS` for performance optimization  
✔️ Simple LOOP & WRITE statements for structured output  

---

## 📜 ABAP Code  
```abap
REPORT ZMATERIAL_REPORT.

TABLES: MARA.

DATA: lt_mara TYPE TABLE OF MARA.

SELECT * FROM MARA INTO TABLE lt_mara UP TO 10 ROWS.

LOOP AT lt_mara INTO DATA(ls_mara).
  WRITE: / ls_mara-MATNR, ls_mara-MTART, ls_mara-MBRSH.
ENDLOOP.
