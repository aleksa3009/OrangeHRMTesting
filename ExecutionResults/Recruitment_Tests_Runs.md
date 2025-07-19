# Execution Results – Recruitment Module  
**Date:** 14-07-2025
**Module:** Recruitment
**Tester:** Aleksa Aleksić
**Browser:** Chrome 138.0.7204.100  
**Environment:** Ubuntu 22.04 LTS   

---

### Recruitment_TC_01: Verify Admin can post a new job vacancy  
**Start Time:** 12:25 
**End Time:** 12:29  
**Status:** PASS  

**Test Steps & Observations:**  
1. Clicked “Add” → Vacancy form displayed.  
2. Entered Job Title, Vacancy Name, Hiring Manager, Number of Positions → Fields accepted input.  
3. Clicked “Save” → Success message shown; vacancy listed.

---

### Recruitment_TC_02: Verify Admin cannot post vacancy without mandatory fields  
**Start Time:** 12:30  
**End Time:** 12:33  
**Status:** PASS  

**Test Steps & Observations:**  
1. Opened Add Vacancy form → OK.  
2. Left Job Title blank → Field marked as required.  
3. Clicked “Save” → Error message shown; form blocked.

---

### Recruitment_TC_03: Verify user can upload CV while applying  
**Start Time:** 12:35  
**End Time:** 12:40  
**Status:** PASS  

**Test Steps & Observations:**  
1. Navigated to Candidate Apply form → Form opened.  
2. Entered Name and Email → Accepted.  
3. Uploaded valid PDF → Upload successful.  
4. Submitted form → Success message displayed; candidate listed.

---

### Recruitment_TC_04: Verify system rejects unsupported file types for CV  
**Start Time:** 12:42  
**End Time:** 12:47  
**Status:** FAIL  

**Test Steps & Observations:**  
1. Tried uploading EXE file → No error shown, file accepted erroneously.  
2. Tried uploading empty file → No validation triggered.  

**Bug:** Unsupported file types not blocked; validation missing.

**Screenshot:**

![Screenshot](/ExecutionResults/Screenshots/BUG-009.png) 

---

### Recruitment_TC_05: Verify Admin can view candidate details  
**Start Time:** 12:48  
**End Time:** 12:51  
**Status:** PASS  

**Test Steps & Observations:**  
1. Opened Candidates list → List displayed.  
2. Clicked candidate name → Details page opened showing info and CV.

---

### Recruitment_TC_06: Verify candidate search filter by status works  
**Start Time:** 12:53  
**End Time:** 12:57  
**Status:** FAIL  

**Test Steps & Observations:**  
1. Opened Candidates list → OK.  
2. Selected filter “Shortlisted” → Shortlisted candidates are not being shown.

**Bug:** Filter "Shortlisted" does not work as intended.

**Screenshot:**

![Screenshot](/ExecutionResults/Screenshots/BUG-010.png) 

---

### Recruitment_TC_07: Verify duplicate candidate resumes cannot be submitted  
**Start Time:** 12:58  
**End Time:** 13:03  
**Status:** FAIL  

**Test Steps & Observations:**  
1. Attempted to re-apply with same name, email, CV as existing candidate → Form submitted successfully.  
2. No error or block on duplicates.  

**Bug:** Duplicate candidate detection missing.

**Screenshot:**

![Screenshot](/ExecutionResults/Screenshots/BUG-011.png) 

---

### Recruitment_TC_08: Verify Recruiter can change candidate status  
**Start Time:** 13:04  
**End Time:** 13:07  
**Status:** PASS  

**Test Steps & Observations:**  
1. Opened candidate record → Detail page loaded.  
2. Changed status to “Shortlisted” → Status updated; confirmation message shown.

---

# Summary
- **Total Test Cases:** 8  
- **Passed:** 5  
- **Failed:** 3  
- **Execution Duration:** 42min (12:25–13:07)

Bugs logged for: Missing validation error (TC_04), "Shortlisted" filter bug (TC_06) and duplicate candidate error (TC_07).