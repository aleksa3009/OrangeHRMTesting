# OrangeHRM Manual Testing – Test Cases

## Admin Module – 12 Test Cases

---

### Admin_TC_01  
**Title:** Verify Admin can create a new user successfully  

**Preconditions:**  
- Logged in as Admin user  
- Admin module page opened  

**Test Steps & Expected Results:**  
1. Navigate to Admin → User Management → Users.  
   - *Expected Result:* Admin Users list page is displayed.  
2. Click “Add” button.  
   - *Expected Result:* Add User form is opened.  
3. Fill in mandatory fields: Username, User Role, Employee Name, Status, Password, Confirm Password.  
   - *Expected Result:* All mandatory fields accept valid inputs without errors.  
4. Click “Save”.  
   - *Expected Result:* New user is added; success message “Successfully Saved” is shown; user appears in the user list.  

**Priority:** High  
**Type:** Functional  

---

### Admin_TC_02  
**Title:** Verify Admin can disable a user account  

**Preconditions:**  
- User account exists and is enabled  
- Logged in as Admin  

**Test Steps & Expected Results:**  
1. Navigate to Admin → User Management → Users.  
   - *Expected Result:* User list page is displayed.  
2. Search and select an active user.  
   - *Expected Result:* Correct user details are displayed.  
3. Click “Edit”.  
   - *Expected Result:* Edit User form is opened.  
4. Change status to “Disabled”.  
   - *Expected Result:* Status dropdown updates to Disabled without error.  
5. Click “Save”.  
   - *Expected Result:* User status is updated to Disabled; success message is shown.  
6. Search for disabled users using filter.  
   - *Expected Result:* Disabled user appears in filtered search results.  

**Priority:** High  
**Type:** Functional  

---

### Admin_TC_03  
**Title:** Verify filtering users by User Role shows correct results  

**Preconditions:**  
- Users with multiple roles exist  
- Logged in as Admin  

**Test Steps & Expected Results:**  
1. Navigate to Admin → User Management → Users.  
   - *Expected Result:* User list page is loaded.  
2. Use “User Role” filter dropdown and select “Admin”.  
   - *Expected Result:* User Role filter is applied with value “Admin”.  
3. Click “Search”.  
   - *Expected Result:* Only users with role “Admin” are displayed; result count matches expected number.  

**Priority:** Medium  
**Type:** Functional  

---

### Admin_TC_04  
**Title:** Verify filtering users by Status shows correct results  

**Preconditions:**  
- Users with varying statuses exist  
- Logged in as Admin  

**Test Steps & Expected Results:**  
1. Navigate to Admin → User Management → Users.  
   - *Expected Result:* User list is displayed.  
2. Select “Disabled” in Status filter dropdown.  
   - *Expected Result:* Status filter set to Disabled.  
3. Click “Search”.  
   - *Expected Result:* Only disabled users are listed in search results.  

**Priority:** Medium  
**Type:** Functional  

---

### Admin_TC_05  
**Title:** Verify Admin can edit user permissions (User Role)  

**Preconditions:**  
- User exists  
- Logged in as Admin  

**Test Steps & Expected Results:**  
1. Navigate to Admin → User Management → Users.  
   - *Expected Result:* Users list displayed.  
2. Search and select a user.  
   - *Expected Result:* User detail page opens.  
3. Click “Edit”.  
   - *Expected Result:* Edit form opens.  
4. Change User Role (e.g., from ESS to Admin).  
   - *Expected Result:* User Role dropdown updates with selected value.  
5. Click “Save”.  
   - *Expected Result:* Changes saved; success message shown; user role updated in list and details.  

**Priority:** High  
**Type:** Functional  

---

### Admin_TC_06  
**Title:** Verify Admin cannot create user with existing username  

**Preconditions:**  
- User “testuser” exists  
- Logged in as Admin  

**Test Steps & Expected Results:**  
1. Navigate to Admin → User Management → Users.  
   - *Expected Result:* User list displayed.  
2. Click “Add”.  
   - *Expected Result:* Add User form opens.  
3. Enter username “testuser”.  
   - *Expected Result:* Username field accepts input.  
4. Fill all mandatory fields.  
   - *Expected Result:* Fields accept valid input.  
5. Click “Save”.  
   - *Expected Result:* Validation error “Username already exists” displayed; user not created.  

**Priority:** High  
**Type:** Negative Functional  

---

### Admin_TC_07  
**Title:** Verify Admin can search user by Username  

**Preconditions:**  
- Users exist  
- Logged in as Admin  

**Test Steps & Expected Results:**  
1. Navigate to Admin → User Management → Users.  
   - *Expected Result:* User list page shown.  
2. Enter username in search box.  
   - *Expected Result:* Search box accepts input.  
3. Click “Search”.  
   - *Expected Result:* Users matching username are displayed; no unrelated users shown.  

**Priority:** Medium  
**Type:** Functional  

---

### Admin_TC_08  
**Title:** Verify pagination in user list works correctly  

**Preconditions:**  
- More than one page of users exists  
- Logged in as Admin  

**Test Steps & Expected Results:**  
1. Navigate to Admin → User Management → Users.  
   - *Expected Result:* User list loaded with pagination controls visible.  
2. Click on pagination controls (Next, Previous).  
   - *Expected Result:* User list updates correctly; page number changes accordingly.  

**Priority:** Low  
**Type:** UI Functional  

---

### Admin_TC_09  
**Title:** Verify Admin can reset user password  

**Preconditions:**  
- User exists  
- Logged in as Admin  

**Test Steps & Expected Results:**  
1. Navigate to Admin → User Management → Users.  
   - *Expected Result:* User list visible.  
2. Search and select user.  
   - *Expected Result:* User detail page opens.  
3. Click “Edit”.  
   - *Expected Result:* Edit form opens.  
4. Enter new password and confirm password.  
   - *Expected Result:* Password fields accept input and match.  
5. Click “Save”.  
   - *Expected Result:* Password updated; success message displayed.  

**Priority:** High  
**Type:** Functional  

---

### Admin_TC_10  
**Title:** Verify Admin cannot create user if mandatory fields are missing  

**Preconditions:**  
- Logged in as Admin  

**Test Steps & Expected Results:**  
1. Navigate to Admin → User Management → Users.  
   - *Expected Result:* User list page displayed.  
2. Click “Add”.  
   - *Expected Result:* Add User form opens.  
3. Leave mandatory fields empty or incomplete.  
   - *Expected Result:* Mandatory fields show validation warnings/errors.  
4. Click “Save”.  
   - *Expected Result:* User creation blocked; error messages displayed.  

**Priority:** High  
**Type:** Negative Functional  

---

### Admin_TC_11  
**Title:** Verify Admin can sort users by Username ascending/descending  

**Preconditions:**  
- Users exist  
- Logged in as Admin  

**Test Steps & Expected Results:**  
1. Navigate to Admin → User Management → Users.  
   - *Expected Result:* User list page loads.  
2. Click Username column header (once).  
   - *Expected Result:* User list sorted ascending alphabetically.  
3. Click Username column header again.  
   - *Expected Result:* User list sorted descending alphabetically.  

**Priority:** Medium  
**Type:** UI Functional  

---

### Admin_TC_12  
**Title:** Verify Admin can deactivate and reactivate a user  

**Preconditions:**  
- User exists and active  
- Logged in as Admin  

**Test Steps & Expected Results:**  
1. Navigate to Admin → User Management → Users.  
   - *Expected Result:* User list displayed.  
2. Select a user, click “Edit”, change status to Disabled.  
   - *Expected Result:* Status dropdown updates; form ready to save.  
3. Click “Save”.  
   - *Expected Result:* User status set to Disabled; success message shown.  
4. Edit same user, change status to Enabled.  
   - *Expected Result:* Status dropdown updates; form ready.  
5. Click “Save”.  
   - *Expected Result:* User status set to Enabled; success message shown.  

**Priority:** High  
**Type:** Functional  

---