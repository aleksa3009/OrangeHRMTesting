# OrangeHRM Manual Testing – Test Cases

## PIM Module – 12 Test Cases

---

### PIM_TC_01  
**Title:** Verify Admin can add a new employee with valid data  

**Preconditions:**  
- Logged in as Admin or PIM user  
- PIM module open  

**Test Steps & Expected Results:**  
1. Navigate to PIM → Employee List.  
   - *Expected Result:* Employee list page is displayed.  
2. Click “Add Employee”.  
   - *Expected Result:* Add Employee form opens.  
3. Fill in mandatory fields: First Name, Last Name, Employee Id.  
   - *Expected Result:* Fields accept valid inputs without errors.  
4. Upload profile picture.  
   - *Expected Result:* Profile picture preview shows successfully.  
5. Click “Save”.  
   - *Expected Result:* Employee is added to list; success message displayed.  

**Priority:** High  
**Type:** Functional  

---

### PIM_TC_02  
**Title:** Verify Admin can edit existing employee details  

**Preconditions:**  
- Employee exists  
- Logged in as Admin or PIM user  

**Test Steps & Expected Results:**  
1. Navigate to PIM → Employee List.  
   - *Expected Result:* Employee list is displayed.  
2. Search and select employee.  
   - *Expected Result:* Employee details page opens.  
3. Click “Edit”.  
   - *Expected Result:* Edit form opens.  
4. Change details (Job Title, Location).  
   - *Expected Result:* Fields accept changes without error.  
5. Click “Save”.  
   - *Expected Result:* Changes saved; updated details shown; success message displayed.  

**Priority:** High  
**Type:** Functional  

---

### PIM_TC_03  
**Title:** Verify Admin can delete an employee record  

**Preconditions:**  
- Employee exists  
- Logged in as Admin or PIM user  

**Test Steps & Expected Results:**  
1. Navigate to PIM → Employee List.  
   - *Expected Result:* Employee list displayed.  
2. Select employee to delete.  
   - *Expected Result:* Employee details or selection ready.  
3. Click “Delete”.  
   - *Expected Result:* Confirmation prompt displayed.  
4. Confirm deletion.  
   - *Expected Result:* Employee removed from list; success message shown.  

**Priority:** High  
**Type:** Functional  

---

### PIM_TC_04  
**Title:** Verify bulk import of employees via CSV  

**Preconditions:**  
- Admin logged in  
- Valid CSV file ready  

**Test Steps & Expected Results:**  
1. Navigate to PIM → Employee List.  
   - *Expected Result:* Employee list page shown.  
2. Click “Import”.  
   - *Expected Result:* Import dialog/modal opens.  
3. Upload CSV file.  
   - *Expected Result:* File accepted without errors.  
4. Confirm import.  
   - *Expected Result:* Employees imported; success message displayed.  

**Priority:** High  
**Type:** Functional  

---

### PIM_TC_05  
**Title:** Verify Admin can upload a profile picture for an employee  

**Preconditions:**  
- Employee exists  
- Logged in as Admin or PIM user  

**Test Steps & Expected Results:**  
1. Navigate to PIM → Employee List.  
   - *Expected Result:* Employee list displayed.  
2. Select employee and open profile.  
   - *Expected Result:* Employee detail page shown.  
3. Click “Edit” and upload profile picture.  
   - *Expected Result:* Picture preview displayed.  
4. Click “Save”.  
   - *Expected Result:* Picture updated; success message shown.  

**Priority:** Medium  
**Type:** Functional  

---

### PIM_TC_06  
**Title:** Verify Admin cannot add employee with duplicate Employee ID  

**Preconditions:**  
- Employee with Employee ID “EMP001” exists  
- Logged in as Admin  

**Test Steps & Expected Results:**  
1. Navigate to PIM → Employee List.  
   - *Expected Result:* Employee list shown.  
2. Click “Add Employee”.  
   - *Expected Result:* Add Employee form opens.  
3. Enter Employee ID “EMP001”.  
   - *Expected Result:* Field accepts input.  
4. Fill other mandatory fields.  
   - *Expected Result:* Fields accept input.  
5. Click “Save”.  
   - *Expected Result:* Validation error “Employee ID already exists”; employee not added.  

**Priority:** High  
**Type:** Negative Functional  

---

### PIM_TC_07  
**Title:** Verify Admin can search employee by name  

**Preconditions:**  
- Employees exist  
- Logged in as Admin or PIM user  

**Test Steps & Expected Results:**  
1. Navigate to PIM → Employee List.  
   - *Expected Result:* Employee list page shown.  
2. Enter employee name in search box.  
   - *Expected Result:* Search box accepts input.  
3. Click “Search”.  
   - *Expected Result:* Employees matching name listed; no unrelated employees shown.  

**Priority:** Medium  
**Type:** Functional  

---

### PIM_TC_08  
**Title:** Verify pagination works in employee list  

**Preconditions:**  
- More than one page of employees exists  
- Logged in as Admin or PIM user  

**Test Steps & Expected Results:**  
1. Navigate to PIM → Employee List.  
   - *Expected Result:* Employee list displayed with pagination.  
2. Use pagination controls.  
   - *Expected Result:* Employee list updates correctly per page; page number updates.  

**Priority:** Low  
**Type:** UI Functional  

---

### PIM_TC_09  
**Title:** Verify Admin can edit employee contact details  

**Preconditions:**  
- Employee exists  
- Logged in as Admin or PIM user  

**Test Steps & Expected Results:**  
1. Navigate to PIM → Employee List.  
   - *Expected Result:* Employee list shown.  
2. Select employee and edit contact info.  
   - *Expected Result:* Contact fields editable.  
3. Click “Save”.  
   - *Expected Result:* Contact info updated; success message shown.  

**Priority:** Medium  
**Type:** Functional  

---

### PIM_TC_10  
**Title:** Verify Admin can deactivate/reactivate an employee  

**Preconditions:**  
- Employee exists and active  
- Logged in as Admin or PIM user  

**Test Steps & Expected Results:**  
1. Navigate to PIM → Employee List.  
   - *Expected Result:* Employee list shown.  
2. Change employee status to inactive.  
   - *Expected Result:* Status updated in UI.  
3. Click “Save”.  
   - *Expected Result:* Status change saved; success message shown.  
4. Change status back to active.  
   - *Expected Result:* Status updated to active in UI.  
5. Click “Save”.  
   - *Expected Result:* Status change saved; success message shown.  

**Priority:** Medium  
**Type:** Functional  

---

### PIM_TC_11  
**Title:** Verify Admin cannot save employee without mandatory fields  

**Preconditions:**  
- Logged in as Admin or PIM user  

**Test Steps & Expected Results:**  
1. Navigate to PIM → Add Employee.  
   - *Expected Result:* Add Employee form opened.  
2. Leave mandatory fields blank.  
   - *Expected Result:* Validation messages shown on mandatory fields.  
3. Attempt to save.  
   - *Expected Result:* Save blocked; employee not added.  

**Priority:** High  
**Type:** Negative Functional  

---

### PIM_TC_12  
**Title:** Verify bulk import rejects invalid CSV rows with error messages  

**Preconditions:**  
- Admin logged in  
- CSV with invalid rows prepared  

**Test Steps & Expected Results:**  
1. Navigate to PIM → Employee List.  
   - *Expected Result:* Employee list page shown.  
2. Click “Import”.  
   - *Expected Result:* Import modal/dialog opens.  
3. Upload invalid CSV file.  
   - *Expected Result:* File accepted, but errors detected.  
4. Review error messages.  
   - *Expected Result:* Invalid rows rejected with clear errors; valid rows imported; summary shown.  

**Priority:** High  
**Type:** Negative Functional  