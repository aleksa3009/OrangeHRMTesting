# Execution Rsults – PIM Module  
**Date:** 14-07-2025  
**Tester:** Aleksa Aleksić  

---

### PIM_TC_01: Verify Admin can add a new employee with valid data  
**Start Time:** 09:30  
**End Time:** 09:36  
**Status:** PASS  

**Test Steps & Observations:**  
1. Navigate to PIM → Employee List → Employee list page is displayed.  
2. Click “Add Employee” → Add Employee form opens.  
3. Fill mandatory fields: `First Name: Mia `, `Last Name: Blake`, `Employee ID: EMP015` → Fields accept input.  
4. Upload profile picture `Mia_Blake.jpeg` → Preview shown correctly.  
5. Click “Save” → Message “Successfully Saved”; employee listed.

---

### PIM_TC_02: Verify Admin can edit existing employee details  
**Start Time:** 09:37  
**End Time:** 09:42  
**Status:** PASS  

**Test Steps & Observations:**  
1. Navigate to PIM → Employee List → Employee list is displayed.  
2. Search “Magdalena Terry” → Employee details page opens.  
3. Click “Edit” → Edit form loads.  
4. Change `Job Title: Product Manager`, `Location: Rome` → Changes accepted.  
5. Click “Save” → Message “Successfully Updated”; new details saved.

---

### PIM_TC_03: Verify Admin can delete an employee record  
**Start Time:** 09:44  
**End Time:** 09:49  
**Status:** PASS  

**Test Steps & Observations:**  
1. Navigate to PIM → Employee List → Employee list displayed.  
2. Select “Test Employee” → Details displayed.  
3. Click “Delete” → Confirmation prompt appears.  
4. Confirm deletion → Success message shown; employee removed from list.

---

### PIM_TC_04: Verify bulk import of employees via CSV  
**Start Time:** 09:50  
**End Time:** 09:54  
**Status:** FAIL  

**Test Steps & Observations:**  
1. Navigate to PIM → Employee List → List loads correctly.  
2. Click “Import” → Modal opens.  
3. Upload file `employees.csv` → File accepted.  
4. Confirm import → Error: “File format not supported.” Import fails.

**Screenshot:**

![Screenshot](/ExecutionResults/Screenshots/BUG-004.png) 

---

### PIM_TC_05: Verify Admin can upload a profile picture for an employee  
**Start Time:** 09:55  
**End Time:** 10:02  
**Status:** PASS  

**Test Steps & Observations:**  
1. Navigate to PIM → Employee List → List loaded.  
2. Select employee “Brad Hines” → Profile opened.  
3. Click “Edit” → Upload picture `Brad_Hines.jpeg` → Preview successful.  
4. Click “Save” → Picture updated; success message shown.

---

### PIM_TC_06: Verify Admin cannot add employee with duplicate Employee ID  
**Start Time:** 10:04  
**End Time:** 10:09  
**Status:** PASS  

**Test Steps & Observations:**  
1. Navigate to PIM → Employee List → List displayed.  
2. Click “Add Employee” → Form opened.  
3. Enter Employee ID `EMP09` → Field accepts input.  
4. Fill other fields and click “Save” → Error: “Employee ID already exists.”

---

### PIM_TC_07: Verify Admin can search employee by name  
**Start Time:** 10:10  
**End Time:** 10:16  
**Status:** PASS  

**Test Steps & Observations:**  
1. Navigate to PIM → Employee List → Page shown.  
2. Enter “Aurora Thomas” in search → Field accepts input.  
3. Click “Search” → Result displayed correctly with exact match.

---

### PIM_TC_08: Verify pagination works in employee list  
**Start Time:** 10:18  
**End Time:** 10:22  
**Status:** PASS  

**Test Steps & Observations:**  
1. Navigate to PIM → Employee List → List displayed with pagination.  
2. Click “Next” → Page 2 loads with new entries.  
3. Click “Previous” → Returns to Page 1.

---

### PIM_TC_09: Verify Admin can edit employee contact details  
**Start Time:** 10:25  
**End Time:** 10:31  
**Status:** PASS  

**Test Steps & Observations:**  
1. Navigate to PIM → Employee List → List shown.  
2. Select “Kelly SMith” and click “Edit” → Fields editable.  
3. Update phone and email → Fields accept changes.  
4. Click “Save” → Contact info saved; message shown.

---

### PIM_TC_10: Verify Admin can deactivate/reactivate an employee  
**Start Time:** 10:32  
**End Time:** 10:37  
**Status:** PASS  

**Test Steps & Observations:**  
1. Navigate to PIM → Employee List → List shown.  
2. Edit employee → Change status to Inactive → Saved successfully.  
3. Reactivate employee → Change to Active → Saved with confirmation.

---

### PIM_TC_11: Verify Admin cannot save employee without mandatory fields  
**Start Time:** 10:39  
**End Time:** 10:43  
**Status:** PASS  

**Test Steps & Observations:**  
1. Navigate to PIM → Add Employee → Form opened.  
2. Leave fields blank → Validation shown.  
3. Click “Save” → Save blocked; error messages shown.

---

### PIM_TC_12: Verify bulk import rejects invalid CSV rows with error messages  
**Start Time:** 10:45  
**End Time:** 10:50  
**Status:** FAIL  

**Test Steps & Observations:**  
1. Navigate to PIM → Employee List → List displayed.  
2. Click “Import” → Modal opened.  
3. Upload file `employees_invalid.csv` → File accepted.  
4. Confirm import → Entire import failed; no detailed error shown.

**Screenshot:**

![Screenshot](/ExecutionResults/Screenshots/BUG-005.png) 

---

# Summary
- **Total Test Cases:** 10  
- **Passed:** 10  
- **Failed:** 2  
- **Execution Duration:** 1h 20m (09:30–10:50)

Bugs logged for: bulk import of employees via CSV (TC_04) and bulk import error (TC_12).