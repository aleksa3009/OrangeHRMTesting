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

## Leave Module – 8 Test Cases

---

### Leave_TC_01  
**Title:** Verify user can apply for future leave  

**Preconditions:**  
- Logged in as Admin or ESS user  
- On Leave → My Leave page  

**Test Steps & Expected Results:**  
1. Click “Apply” button.  
   - *Expected Result:* Apply Leave form opens.  
2. Select “From Date” = tomorrow’s date, “To Date” = day after tomorrow.  
   - *Expected Result:* Date pickers accept future dates.  
3. Choose Leave Type (e.g., “Annual Leave”).  
   - *Expected Result:* Leave Type dropdown accepts selection.  
4. Enter “Leave Balance” remark field.  
   - *Expected Result:* Remarks field accepts text.  
5. Click “Save”.  
   - *Expected Result:* Leave request saved; confirmation message “Successfully Saved” appears; new entry shown in My Leave list.  

**Priority:** High  
**Type:** Functional  

---

### Leave_TC_02  
**Title:** Verify user cannot apply for past leave  

**Preconditions:**  
- Logged in as ESS user  
- On Leave → My Leave page  

**Test Steps & Expected Results:**  
1. Click “Apply”.  
   - *Expected Result:* Apply Leave form opens.  
2. Select “From Date” and “To Date” both in the past.  
   - *Expected Result:* Date picker prevents selecting past dates or shows validation.  
3. Click “Save”.  
   - *Expected Result:* Validation error “From date cannot be in the past” displayed; form not submitted.  

**Priority:** Medium  
**Type:** Negative Functional  

---

### Leave_TC_03  
**Title:** Verify user cannot apply leave without selecting mandatory fields  

**Preconditions:**  
- Logged in as ESS user  
- On Apply Leave form  

**Test Steps & Expected Results:**  
1. Open Apply Leave form.  
   - *Expected Result:* Form opens.  
2. Leave “From Date” and/or “To Date” blank.  
   - *Expected Result:* Blank fields flagged as required.  
3. Click “Save”.  
   - *Expected Result:* Validation messages “Required” appear next to blank fields; leave not applied.  

**Priority:** High  
**Type:** Negative Functional  

---

### Leave_TC_04  
**Title:** Verify overlapping leave request is rejected  

**Preconditions:**  
- A leave request exists in date range July 20–22, 2025  
- Logged in as ESS user  

**Test Steps & Expected Results:**  
1. Open Apply Leave form.  
   - *Expected Result:* Form opens.  
2. Select “From Date” = May 21, 2025 and “To Date” = May 23, 2025.  
   - *Expected Result:* Date pickers accept input.  
3. Click “Save”.  
   - *Expected Result:* Error “You already have a leave request in this period” displayed; form not submitted.  

**Priority:** High  
**Type:** Functional  

---

### Leave_TC_05  
**Title:** Verify user can cancel an approved leave  

**Preconditions:**  
- An approved leave exists for current month  
- Logged in as ESS user  

**Test Steps & Expected Results:**  
1. Navigate to Leave → My Leave.  
   - *Expected Result:* My Leave list displays past and pending requests.  
2. Find approved leave entry and click “Cancel”.  
   - *Expected Result:* Confirmation dialog appears.  
3. Confirm cancellation.  
   - *Expected Result:* Status changes to “Cancelled”; success message displayed.  

**Priority:** Medium  
**Type:** Functional  

---

### Leave_TC_06  
**Title:** Verify leave balance updates after applying leave  

**Preconditions:**  
- User has leave balance ≥ 5 days  
- Logged in as ESS user  

**Test Steps & Expected Results:**  
1. Note current leave balance on My Leave page.  
   - *Expected Result:* Balance is displayed (e.g., “10 days”).  
2. Apply for 2-day leave in the future.  
   - *Expected Result:* Leave applied successfully.  
3. Refresh My Leave page.  
   - *Expected Result:* Leave balance reduced by 2 days (e.g., now “8 days”).  

**Priority:** High  
**Type:** Functional  

---

### Leave_TC_07  
**Title:** Verify error message when leave type is not selected  

**Preconditions:**  
- Logged in as ESS user  
- Apply Leave form open  

**Test Steps & Expected Results:**  
1. Select valid “From Date” and “To Date”.  
   - *Expected Result:* Dates accepted.  
2. Leave “Leave Type” blank.  
   - *Expected Result:* Leave Type dropdown shows placeholder.  
3. Click “Save”.  
   - *Expected Result:* Validation error “This field is required” shown near Leave Type.  

**Priority:** High  
**Type:** Negative Functional  

---

### Leave_TC_08  
**Title:** Verify overlap check for partial overlaps  

**Preconditions:**  
- Existing pending leave July 20–22, 2025  
- Logged in as ESS user  

**Test Steps & Expected Results:**  
1. Open Apply Leave form.  
   - *Expected Result:* Form visible.  
2. Select “From Date” = July 22, 2025 and “To Date” = July 24, 2025.  
   - *Expected Result:* Dates accepted.  
3. Click “Save”.  
   - *Expected Result:* Warning “Overlap with existing leave request” displayed; block submission.  

**Priority:** High  
**Type:** Functional  

---

## Recruitment Module – 8 Test Cases

### Recruitment_TC_01  
**Title:** Verify Admin can post a new job vacancy  

**Preconditions:**  
- Logged in as Admin  
- On Recruitment → Vacancies page  

**Test Steps & Expected Results:**  
1. Click “Add” to create a new vacancy.  
   - *Expected Result:* Add Vacancy form is displayed.  
2. Enter Job Title, Vacancy Name, Hiring Manager, and Number of Positions.  
   - *Expected Result:* Fields accept input.  
3. Click “Save”.  
   - *Expected Result:* Vacancy saved; success message shown; vacancy appears in list.  

**Priority:** High  
**Type:** Functional  

---

### Recruitment_TC_02  
**Title:** Verify Admin cannot post vacancy without mandatory fields  

**Preconditions:**  
- Logged in as Admin  

**Test Steps & Expected Results:**  
1. Navigate to Add Vacancy form.  
   - *Expected Result:* Form is displayed.  
2. Leave Job Title or Vacancy Name blank.  
   - *Expected Result:* Required fields are marked.  
3. Click “Save”.  
   - *Expected Result:* Error message shown; form not submitted.  

**Priority:** High  
**Type:** Negative Functional  

---

### Recruitment_TC_03  
**Title:** Verify user can upload CV while applying  

**Preconditions:**  
- Recruitment module enabled  

**Test Steps & Expected Results:**  
1. Navigate to Careers or Recruitment → Candidates.  
   - *Expected Result:* Candidate form opens.  
2. Fill in Name and Email.  
   - *Expected Result:* Fields accept valid input.  
3. Upload a valid PDF or DOC file.  
   - *Expected Result:* File uploads successfully.  
4. Submit form.  
   - *Expected Result:* Success message appears; candidate listed.  

**Priority:** High  
**Type:** Functional  

---

### Recruitment_TC_04  
**Title:** Verify system rejects unsupported file types for CV  

**Preconditions:**  
- On Candidate Apply form  

**Test Steps & Expected Results:**  
1. Attempt to upload EXE file as CV.  
   - *Expected Result:* Error message “Unsupported file type” shown.  
2. Attempt to upload empty file.  
   - *Expected Result:* Validation error or ignored.  

**Priority:** High  
**Type:** Negative Functional  

---

### Recruitment_TC_05  
**Title:** Verify Admin can view candidate details  

**Preconditions:**  
- Candidate already submitted application  

**Test Steps & Expected Results:**  
1. Navigate to Recruitment → Candidates.  
   - *Expected Result:* Candidate list is shown.  
2. Click on candidate name.  
   - *Expected Result:* Details page opens with name, contact info, CV.  

**Priority:** Medium  
**Type:** Functional  

---

### Recruitment_TC_06  
**Title:** Verify candidate search filter by status works  

**Preconditions:**  
- Multiple candidates in system with various statuses  

**Test Steps & Expected Results:**  
1. Go to Candidates list.  
   - *Expected Result:* List is shown.  
2. Select filter “Shortlisted”.  
   - *Expected Result:* Only shortlisted candidates are shown.  

**Priority:** Medium  
**Type:** Functional  

---

### Recruitment_TC_07  
**Title:** Verify duplicate candidate resumes cannot be submitted  

**Preconditions:**  
- Candidate “John Smith” already exists  

**Test Steps & Expected Results:**  
1. Re-apply using same name, email, and CV.  
   - *Expected Result:* Error “Candidate already exists” or blocked.  

**Priority:** Medium  
**Type:** Negative Functional  

---

### Recruitment_TC_08  
**Title:** Verify Recruiter can change candidate status  

**Preconditions:**  
- Logged in as Recruiter  
- Candidate in “Application Received” status  

**Test Steps & Expected Results:**  
1. Open candidate record.  
   - *Expected Result:* Candidate detail page opens.  
2. Change status to “Shortlisted”.  
   - *Expected Result:* Status is updated; confirmation message displayed.  

**Priority:** Medium  
**Type:** Functional  

---

## Exploratory Module – 5 Test Cases

### Exploratory_TC_01  
**Title:** Verify navigation through top bar tabs does not break layout  

**Preconditions:**  
- Logged in as Admin  

**Test Steps & Expected Results:**  
1. Click all top navigation tabs rapidly.  
   - *Expected Result:* Pages load correctly; no layout breakage.  

**Priority:** Medium  
**Type:** Exploratory  

---

### Exploratory_TC_02  
**Title:** Verify handling of invalid filter input  

**Preconditions:**  
- On Employee List page  

**Test Steps & Expected Results:**  
1. Enter invalid characters in name search.  
   - *Expected Result:* No crash; shows “No records found”.  

**Priority:** Medium  
**Type:** Negative Functional  

---

### Exploratory_TC_03  
**Title:** Verify long input in search filters does not break UI  

**Preconditions:**  
- On Admin → User Management page  

**Test Steps & Expected Results:**  
1. Paste 255-character string into Username field.  
   - *Expected Result:* Field accepts input but UI remains intact.  

**Priority:** Medium  
**Type:** UI  

---

### Exploratory_TC_04  
**Title:** Verify combo filters return correct result  

**Preconditions:**  
- On Employee List page  

**Test Steps & Expected Results:**  
1. Select Job Title = “QA Engineer” and Sub Unit = “IT”.  
   - *Expected Result:* Filter returns employees matching both conditions.  

**Priority:** Medium  
**Type:** Functional  

---

### Exploratory_TC_05  
**Title:** Verify app behavior when session times out  

**Preconditions:**  
- Logged in and idle for 30+ minutes  

**Test Steps & Expected Results:**  
1. Try to perform any action after timeout.  
   - *Expected Result:* Redirected to login page; session expired message shown.  

**Priority:** Medium  
**Type:** Exploratory 
