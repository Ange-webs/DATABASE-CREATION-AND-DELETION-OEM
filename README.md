Oracle Pluggable Database (PDB) Practical

## Student Information
**Name:** Uwimbabazi Ange  
**Student ID:** 27629  
**Course:** PL/SQL and Database Administration  



## 📘 Overview

This project demonstrates how to:
1. **Create a new Pluggable Database (PDB)**  
2. **Create and delete another PDB**  
3. **Configure and access Oracle Enterprise Manager (OEM Express)**  

All tasks were performed in **Oracle Database 21c Express Edition (XE)** on **Windows**.

---

##  Task 1: Create a New PDB

### Steps
1. Connect as SYSDBA and switch to root container:
   ```sql
   sqlplus / as sysdba
   ALTER SESSION SET CONTAINER=CDB$ROOT;
   SHOW CON_NAME;
CREATE PLUGGABLE DATABASE AN_PDB_27629
ADMIN USER ANGE_PLSQLAUCA_27629 IDENTIFIED BY 12345
FILE_NAME_CONVERT=(
  'C:\\app\\maris\\product\\21c\\oradata\\XE\\pdbseed\\',
  'C:\\app\\maris\\product\\21c\\oradata\\XE\\AN_PDB_27629\\'
);

CREATE PLUGGABLE DATABASE AN_PDB_27629
ADMIN USER ANGE_PLSQLAUCA_27629 IDENTIFIED BY 12345
FILE_NAME_CONVERT=(
  'C:\\app\\maris\\product\\21c\\oradata\\XE\\pdbseed\\',
  'C:\\app\\maris\\product\\21c\\oradata\\XE\\AN_PDB_27629\\'
);

ALTER PLUGGABLE DATABASE AN_PDB_27629 OPEN;
ALTER PLUGGABLE DATABASE AN_PDB_27629 SAVE STATE;
SHOW PDBS;
ALTER PLUGGABLE DATABASE AN_PDB_27629 OPEN;
ALTER PLUGGABLE DATABASE AN_PDB_27629 SAVE STATE;
SHOW PDBS;

