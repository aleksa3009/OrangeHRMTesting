# Final Report – OrangeHRM Live Manual Testing Project

**Project:** Manual Testing of OrangeHRM Live Demo HR Portal\
**Tester:** Aleksa Aleksić\
**Duration:** 12-07-2025 to 16-07-2025\
**Base URL:** [https://opensource-demo.orangehrmlive.com](https://opensource-demo.orangehrmlive.com)

---

## 1. Introduction

This report summarizes the comprehensive manual testing efforts on the OrangeHRM Live demo portal. Over six days, we executed functional, negative, and exploratory tests across key HR modules to validate core features and identify defects.

**Modules Tested:** Admin, PIM, Leave, Recruitment, Dashboard, Exploratory

**Artifacts Produced:** Test Plan, 50 Test Cases, Execution Logs, 12 Defect Reports, Exploratory Report, Daily Reports

---

## 2. Scope & Objectives

**Scope:**

- Functional validation of five HR modules and end-to-end workflows
- Negative testing: missing input, boundary values, duplicate entries
- Exploratory testing: UI boundaries, invalid file uploads, deep linking

**Objectives:**

1. Verify module behaviors under normal and adverse conditions
2. Detect and document functional and UI defects
3. Produce reusable QA artifacts suitable for portfolio
4. Practice bug reporting using GitHub Issues

---

## 3. Test Environment & Tools

**OS:** Ubuntu 22.04 LTS
**Browsers:** Chrome 138.0.7204.100
**Test Management:** Markdown, LibreOffice Calc, TestRail
**Bug Tracking:** GitHub Issues
**Screenshots:** Lightshot & LibreOffice Draw
**Version Control:** Git & GitHub

---

## 4. Folder Structure & Artifacts

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

## 5. Test Case Coverage & Metrics

| Module      | Test Cases | PASS | FAIL | Bugs Logged |
| ----------- | ---------- | ---- | ---- | ----------- |
| Admin       | 12         | 9    | 3    | 3           |
| PIM         | 12         | 10   | 2    | 2           |
| Leave       | 8          | 5    | 3    | 3           |
| Recruitment | 8          | 5    | 3    | 3           |
| Dashboard   | 5          | 4    | 1    | 1           |
| Exploratory | 6          | 6    | 0    | 0           |
| **Total**   | 51         | 43   | 8    | 12          |

- **Execution Duration:** 5 days
- **Average per TC:** \~10 min
- **Total Defects:** 12

---

## 6. Defect Analysis

**High Severity (4):**

- Duplicate username allowed
- Past leave requests accepted
- Unsupported file uploads initially accepted
- Missing leave balance update

**Medium Severity (6):**

- Bulk CSV import error handling
- Duplicate candidate detection
- Password reset not applied initially
- Filter inconsistencies
- Pagination/UI alignment

**Low Severity (2):**

- Dashboard responsive layout on smaller screens
- Minor UI spacing issues

**Root Causes:** Input validation gaps, inconsistent UI feedback, partial backend checks

---

## 7. Exploratory Testing Insights

1. Leap year date handling verified.
2. Invalid input sanitization (HTML injection, whitespace).
3. Edge file uploads properly validated.
4. Cancel workflows close forms without data retention.
5. Deep linking unauthorized access handled gracefully.
6. Stress navigation produced no crashes.

---

## 8. Lessons Learned & Recommendations

1. **Strengthen Frontend Validation:** Block invalid inputs early.
2. **Enhance CSV Import UX:** Row-level error messages for bulk operations.
3. **Implement Duplicate Detection:** Enforce unique constraints client-side.
4. **Consistent Feedback:** Standardize success/error messaging.
5. **Responsive Design:** Test and fix UI on all supported resolutions.

---

## 9. Conclusion

This project demonstrates a robust manual testing practice for a complex HR portal. Deliverables include detailed test artifacts, reproducible defect reports, and exploratory findings—showcasing comprehensive QA capabilities ideal for a junior tester portfolio.

All materials are ready for review in this repository. Thank you for exploring my work!
