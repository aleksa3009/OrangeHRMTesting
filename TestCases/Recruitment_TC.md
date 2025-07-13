# OrangeHRM Manual Testing – Test Cases

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