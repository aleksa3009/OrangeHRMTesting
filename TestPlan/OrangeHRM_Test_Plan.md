# Test Plan: OrangeHRM Live – HR Portal Functional Testing  

**Author:** Aleksa Aleksić  
**Date:** July 12, 2025  
**Project:** OrangeHRM Live – HR Portal Functional Testing  
**Base URL:** https://opensource-demo.orangehrmlive.com  

---

## 1. Introduction  
This document defines the formal test plan for conducting functional testing of the OrangeHRM Live demo portal. The objective is to validate key HR modules, simulate real-world scenarios, and detect any functional or UI defects. A total of 50 test cases (including positive and negative flows) will be executed, resulting in QA deliverables suitable for a professional portfolio.

---

## 2. Scope  

**In Scope:**  
- Functional testing of the following modules:  
  - **Admin:** User and role management, access control, filtering  
  - **PIM:** Employee data management, photo upload, CSV bulk import  
  - **Leave:** Request, cancel, and validate leave types; overlap handling  
  - **Recruitment:** Create job vacancies, upload CVs, track applications  
  - **Dashboard:** Validate widgets, quick links, summary data  
  - **Exploratory:** Random navigation, UI boundary cases, filter stress tests  
- End-to-end workflows (e.g., create employee → assign leave → review dashboard)  
- Negative flows (e.g., uploading unsupported file types, missing mandatory fields)  
- Bug reporting via GitHub Issues (approximately 15 expected defect tickets)

**Out of Scope:**  
- API or automated test execution  
- Extensive performance/load testing beyond basic responsiveness checks  
- Security or accessibility testing  

---

## 3. Objectives  
- Verify that each module meets its functional and UI requirements  
- Identify, document, and report defects with reproducible steps and screenshots  
- Produce comprehensive QA artifacts: Test Plan, Test Cases, Bug Reports, Execution Results  
- Utilize GitHub Issues for bug tracking and reporting practices  
- Complete all testing activities within six (6) workdays, ready for inclusion in a QA portfolio

---

## 4. Roles & Responsibilities  

| Role        | Name            | Responsibility                                        |
|-------------|-----------------|-------------------------------------------------------|
| Tester      | Aleksa Aleksić  | Draft test plan, execute test cases, log defects      |
| Reviewer    | Self            | Review QA artifacts and provide feedback              |
| Stakeholder | Product Owner   | Triage reported defects and review final deliverables |

---

## 5. Test Items  

| Module       | Description                                                        |
|--------------|--------------------------------------------------------------------|
| Admin        | Add/Edit/Delete user accounts; assign roles; search & filtering     |
| PIM          | Add/Edit/Delete employee records; photo upload; CSV import         |
| Leave        | Submit/cancel leave requests; validate overlaps and error messages |
| Recruitment  | Post job openings; upload and review CVs; track application status  |
| Dashboard    | Verify dashboard widgets, quick links, and summary statistics      |
| Exploratory  | Random navigation; UI boundary conditions; stress filter scenarios |

---

## 6. Test Approach & Strategy  
1. **Test Types:** Functional, UI, negative, boundary, exploratory  
2. **Design:** Risk-based coverage of happy paths and error conditions  
3. **Data-Driven:** Use `TestData/employees.csv` containing 20 diverse employee records, including edge cases  
4. **Execution Order:**  
   1. Admin  
   2. PIM  
   3. Leave  
   4. Recruitment  
   5. Dashboard  
   6. Exploratory  
5. **Browsers:** Chrome (latest), Firefox (latest)  
6. **Defect Management:** GitHub Issues with standardized labels (`severity`, `module`, `type`)  
7. **Evidence Capture:** Lightshot + LibreOffice Draw annotations  
8. **Documentation:**  
   - Test Plan: Markdown (`TestPlan/OrangeHRM_Test_Plan.md`)  
   - Test Cases: Excel (`TestCases/OrangeHRM_TC.xlsx`)  
   - Execution Logs: Markdown (`ExecutionResults/Module_Results_<module>.md`)

---

## 7. Environment & Tools  
- **Browsers:** Chrome & Firefox (latest)  
- **Devices:** Desktop only (no mobile emulation)  
- **Test Data:**  
  - `TestData/employees.csv` (20 records with columns: FirstName, LastName, EmployeeID, JobTitle, Location, ProfilePic)  
- **Bug Tracking:** GitHub Issues in `OrangeHRMTesting` repo  
- **Screenshots:** Lightshot for capture, LibreOffice Draw for annotations  
- **Version Control:** Git + GitHub  
- **Editor:** VS Code for Markdown, Excel for TC spreadsheet

---

## 8. Entry Criteria  
- Repository initialized with correct folder structure  
- `employees.csv` and `profile_pics/` populated with test data  
- Test Plan template available in Markdown  
- GitHub Issues board configured with issue templates and labels  
- Testing tools installed and configured

---

## 9. Exit Criteria  
- All 50 test cases executed and marked PASS/FAIL in execution logs  
- ~15 defects logged in GitHub Issues with full reproduction steps and screenshots  
- Daily reports created for Days 1–5 (`Reports/Daily_Report_<YYYY-MM-DD>.md`)  
- Final Report (`Reports/Final_Report.md`) completed, including:  
  - Test summary  
  - Pass/fail metrics  
  - Defect density and severity distribution  
  - Lessons learned

---

## 10. Risks & Mitigation  

| Risk                                    | Likelihood | Impact | Mitigation                                     |
|-----------------------------------------|------------|--------|------------------------------------------------|
| UI changes on the portal                | Medium     | High   | Perform daily smoke checks; update test steps  |
| Invalid test data for CSV import        | Low        | Medium | Validate CSV format before execution           |
| Flaky behavior during photo uploads     | Medium     | Medium | Implement retry logic; test multiple formats   |
| Delays in GitHub workflow or triage     | Low        | Low    | Use templates and automation for issue labels  |

---

## 11. Deliverables  
- **Test Plan:** `TestPlan/OrangeHRM_Test_Plan.md`  
- **Test Cases:** `TestCases/OrangeHRM_TC.xlsx`  
- **Test Data:** `TestData/employees.csv` + `profile_pics/`  
- **Execution Results:** `ExecutionResults/Module_Results_<module>.md`  
- **Bug Reports:** GitHub Issues (~15)  
- **Daily Reports:** `Reports/Daily_Report_<YYYY-MM-DD>.md` (5 files)  
- **Final Report:** `Reports/Final_Report.md`

---

## 12. Schedule  
| Day | Activity                                                                           | Duration |
|-----|------------------------------------------------------------------------------------|----------|
| 1   | Setup & initial planning; create `employees.csv`; draft first 15 TC for Admin & PIM | 4 h      |
| 2   | Complete all 50 test cases; configure GitHub Issues; review coverage               | 4 h      |
| 3   | Execute Admin & PIM test cases (24); log ~6 defects; capture screenshots           | 5 h      |
| 4   | Execute Leave & Recruitment test cases (16); edge-case validations; log 4–5 defects  | 5 h      |
| 5   | Execute Dashboard (5) & Exploratory (5) test cases; retest fixed defects            | 4 h      |
| 6   | Clean up GitHub Issues (assign severity/status); draft `Final_Report.md`; portfolio README | 5 h      |
