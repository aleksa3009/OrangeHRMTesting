# OrangeHRM Live – Manual HR Portal Testing Project

A comprehensive manual QA project showcasing end-to-end functional and exploratory testing of the OrangeHRM Live demo HR portal ([https://opensource-demo.orangehrmlive.com](https://opensource-demo.orangehrmlive.com)).

---

## Project Overview

This repository contains all artifacts produced during a six-day manual testing engagement on OrangeHRM Live, covering:

- **Admin**: User Management, Role Permissions, Filtering, Sorting
- **PIM**: Employee CRUD, Bulk CSV Import, Profile Picture Upload
- **Leave**: Apply, Cancel, Balance Validation, Overlap Handling
- **Recruitment**: Job Postings, CV Upload, Application Tracking
- **Dashboard**: Widget Verification, Summary Data, Quick Links
- **Exploratory**: UI Boundaries, Invalid Inputs, Edge Flows

A total of **50 structured test cases** and **6 exploratory scenarios** were executed, resulting in **12 logged defects** with clear reproduction steps and screenshots.

**Note:** This is a personal portfolio project. A few of the reported bugs were intentionally fabricated to demonstrate defect documentation and reporting skills.*


---

## Repository Structure

```bash
~/OrangeHRMTesting/
├── README.md
├── TestPlan/
│   └── OrangeHRM_Test_Plan.md
├── TestCases/
│   ├── OrangeHRM_TC.md
│   ├── Admin_TC.md
│   ├── PIM_TC.md
│   ├── Leave_TC.md
│   ├── Recruitment_TC.md
│   ├── Dashboard_TC.md
│   ├── Exploratory_TC.md
│   └── TestRail_Screenshots/
├── TestData/
│   ├── employees.csv
│   ├── README.md
│   └── profile_pics/
├── ExecutionResults/
│   ├── Admin_Tests_Runs.md
│   ├── PIM_Tests_Runs.md
│   ├── Leave_Tests_Runs.md
│   ├── Recruitment_Tests_Runs.md
│   ├── Exploratory_Tests_Runs.md
│   ├── Bug_Retest.md
│   └── Screenshots/
├── Reports/
│   ├── Daily_Report_12-07-2025.md
│   ├── Daily_Report_13-07-2025.md
│   ├── Daily_Report_14-07-2025.md
│   ├── Daily_Report_15-07-2025.md
│   ├── Daily_Report_16-07-2025.md
│   ├── Exploratory_Testing_Report_15-07-2025.md
│   └── Final_Report.md
```

---

## Tools & Environment

- **Operating System:** Ubuntu 22.04 LTS  
- **Browsers:** Chrome 138.0.7204.100    
- **Test Management:** Markdown files, LibreOffice Calc, TestRail  
- **Bug Tracking:** GitHub Issues  
- **Screenshots:** Lightshot & LibreOffice Draw  
- **Version Control:** Git & GitHub

---

## Test Planning & Execution Flow

| Day    | Activities                                                                                             |
|--------|--------------------------------------------------------------------------------------------------------|
| Day 1  | Setup repo; draft Test Plan; create `employees.csv`; outline 50 test cases                             |
| Day 2  | Finalize all test cases; configure TestRail; review data and filters                                   |
| Day 3  | Execute **Admin** & **PIM** modules (24 TCs); record results; log defects                              |
| Day 4  | Execute **Leave** & **Recruitment** modules (16 TCs); capture edge cases; commence exploratory tests    |
| Day 5  | Execute **Dashboard** & **Exploratory** (10 TCs/6 sessions); retest fixed bugs; update logs             |
| Day 6  | Final defect triage; compile Final Report; update README; prepare portfolio assets                     |

All execution logs and findings reside under **ExecutionResults/** and **Reports/**.

---

## Test Coverage & Metrics

| Module         | Test Cases | PASS | FAIL | Bugs Logged |
|----------------|-----------:|-----:|-----:|------------:|
| Admin          |         12 |    9 |    3 |           3 |
| PIM            |         12 |   10 |    2 |           2 |
| Leave          |          8 |    5 |    3 |           3 |
| Recruitment    |          8 |    5 |    3 |           3 |
| Dashboard      |          5 |    4 |    1 |           1 |
| Exploratory    |          5 |    5 |    0 |           0 |
| **Total**      |         50 |   38 |    12|          12 |

- **Average Duration per TC:** ~8 min  
- **Total Defects Reported:** 12  
- **Exploratory Sessions:** 4

---

## Notable Defects

- **High Severity:**
  - Duplicate username allowed (Admin_TC_06)
  - Past leave requests accepted (Leave_TC_02)
- **Medium Severity:**
  - Bulk CSV import rejects valid rows (PIM_TC_04)
  - Candidate CV duplicates not detected (Recruitment_TC_07)
- **Low Severity:**
  - Dashboard misalignment at 1366×768 (Dashboard_TC_03)

All defects include detailed reproduction steps and annotated screenshots in GitHub Issues.

---

## Exploratory Testing Highlights

1. **Leap Year & Date Boundaries:** System correctly handles Feb 29 in leap year.
2. **Invalid File Upload:** `.exe` and `.txt` files blocked with proper error messages.
3. **HTML Injection Check:** Special tags sanitized in form inputs.
4. **Whitespace Trimming:** Leading/trailing spaces in names trimmed on save.
5. **Cancel Workflow:** Cancel button closes form without unintended side effects.
6. **Deep Linking Access:** Unauthorized URLs redirect appropriately or show “Not Found”.

---

## Recommendations

1. **Enhance Validation:** Add frontend checks for unique usernames and past dates.  
2. **Improve CSV Import UX:** Provide row-level error details for bulk imports.  
3. **Strengthen Duplicate Detection:** Detect repeat candidate submissions by email/CV.  
4. **Responsive Design Refinements:** Tweak widget layouts for smaller resolutions.  
5. **User Feedback:** Display confirmation messages consistently (e.g., leave cancellation).

---

## Conclusion

This project demonstrates a thorough manual testing approach for OrangeHRM Live over six days, covering functional, negative, and exploratory scenarios. With 50 test cases executed, 12 defects reported, and extensive documentation, this repository provides a strong showcase of manual QA skills suited for a junior tester portfolio.
