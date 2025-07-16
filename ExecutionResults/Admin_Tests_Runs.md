# Execution Results – Admin Module

**Date:** 14-07-2025  
**Module:** Admin  
**Executed by:** Aleksa Aleksić  
**Browser:** Chrome 138.0.7204.100  
**Environment:** Ubuntu 22.04 LTS

---

### Admin_TC_01: Verify Admin can create a new user successfully  
**Start Time:** 08:00  
**End Time:** 08:08  
**Status:** PASS  

**Test Steps & Observations:**  
1. Navigate to Admin → User Management → Users → Users list displayed correctly.  
2. Click “Add” → Add User form opened.  
3. Fill all mandatory fields (Username: `testuser1`, Role: `ESS`, Employee Name: `John Doe`, Status: `Enabled`, Password: `Pass@123`) → All inputs accepted.  
4. Click “Save” → Message "Successfully Saved" appeared; user listed.  

---

### Admin_TC_02: Verify Admin can disable a user account  
**Start Time:** 08:10  
**End Time:** 08:16  
**Status:** PASS  

**Test Steps & Observations:**  
1. Navigate to Users → Displayed correctly.  
2. Search for `testuser1`, click Edit → Edit form shown.  
3. Change status to “Disabled” → Dropdown accepted change.  
4. Click “Save” → Success message shown.  
5. Filter by Disabled → `testuser1` appears in filtered results.  

---

### Admin_TC_03: Verify filtering users by User Role shows correct results  
**Start Time:** 08:17  
**End Time:** 08:22  
**Status:** PASS  

**Test Steps & Observations:**  
1. Go to Users page → Loaded properly.  
2. Select Role = Admin → Filter applied.  
3. Click Search → Only Admins listed.  

---

### Admin_TC_04: Verify filtering users by Status shows correct results  
**Start Time:** 08:24  
**End Time:** 08:29  
**Status:** PASS  

**Test Steps & Observations:**  
1. Open Users page → Displayed.  
2. Select Status = Disabled → Filter applied.  
3. Click Search → Disabled users listed.  

---

### Admin_TC_05: Verify Admin can edit user permissions (User Role)  
**Start Time:** 08:30  
**End Time:** 08:36  
**Status:** PASS  

**Test Steps & Observations:**  
1. Navigate to Users → List displayed.  
2. Search `testuser1`, click Edit → Edit form shown.  
3. Change Role to Admin → Dropdown updated.  
4. Click Save → Role changed; success message appeared.  

---

### Admin_TC_06: Verify Admin cannot create user with existing username  
**Start Time:** 08:37  
**End Time:** 08:40  
**Status:** FAIL  

**Test Steps & Observations:**  
1. Click Add → Form opened.  
2. Enter username `testuser1` → Accepted.  
3. Fill all fields → Inputs valid.  
4. Click Save → No validation error shown; user was re-created 

**Bug logged: Duplicate username allowed.**  

**Screenshot:**

![Screenshot](/ExecutionResults/Screenshots/BUG-001.png)

---

### Admin_TC_07: Verify Admin can search user by Username  
**Start Time:** 08:41  
**End Time:** 08:45  
**Status:** PASS  

**Test Steps & Observations:**  
1. Navigate to Users → Page shown.  
2. Enter `testuser1` → Search input accepted.  
3. Click Search → Matching user displayed.  

---

### Admin_TC_08: Verify pagination in user list works correctly  
**Start Time:** 08:47  
**End Time:** 08:53  
**Status:** PASS  

**Test Steps & Observations:**  
1. Open Users list → Pagination visible.  
2. Click Next → Page changed.  
3. Click Previous → Back to first page.  

---

### Admin_TC_09: Verify Admin can reset user password  
**Start Time:** 08:55  
**End Time:** 09:01  
**Status:** FAIL  

**Test Steps & Observations:**  
1. Search user `testuser2`, click Edit → Form shown.  
2. Enter new password and confirm → Fields accepted.  
3. Click Save → Message shown, but password didn't update on login retry  

**Bug logged: Password reset not applied.**

**Screenshot:**

![Screenshot](/ExecutionResults/Screenshots/BUG-002.png)  

---

### Admin_TC_10: Verify Admin cannot create user if mandatory fields are missing  
**Start Time:** 09:02  
**End Time:** 09:06  
**Status:** PASS  

**Test Steps & Observations:**  
1. Click Add → Form opened.  
2. Leave all fields blank → Validation triggered.  
3. Click Save → Error messages shown; user not created.  

---

### Admin_TC_11: Verify Admin can sort users by Username ascending/descending  
**Start Time:** 09:07  
**End Time:** 09:12  
**Status:** PASS  

**Test Steps & Observations:**  
1. Click Username header once → Sorted ascending.  
2. Click again → Sorted descending.  

---

### Admin_TC_12: Verify Admin can deactivate and reactivate a user  
**Start Time:** 09:13  
**End Time:** 09:17  
**Status:** FAIL  

**Test Steps & Observations:**  
1. Edit user `testuser5`, set status to Disabled → Saved.  
2. Edit again, set to Enabled → Save fails with error: "Invalid status update."

**Bug logged: Reactivation fails with error**

**Screenshot:**

![Screenshot](/ExecutionResults/Screenshots/BUG-003.png) 

---

# Summary
- **Total Test Cases:** 12  
- **Passed:** 9  
- **Failed:** 3  
- **Execution Duration:** 1h 17m (08:00–09:17)

Bugs logged for: duplicate username (TC_06), password reset failure (TC_09), and status toggle error (TC_12).
