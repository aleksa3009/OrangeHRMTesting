# OrangeHRM Live – HR Portal Functional Testing

## Project Overview
This manual QA project covers functional testing of the OrangeHRM Live demo portal ([https://opensource-demo.orangehrmlive.com](https://opensource-demo.orangehrmlive.com)), focusing on five key HR modules and end-to-end user workflows. The aim is to simulate real HR operations and detect defects across features with a total of 50 test cases.

## Modules Tested
- Admin: User and role management, access control, filters
- PIM: Employee data management, photo upload, bulk CSV import
- Leave: Apply, cancel, validate leave, overlap handling
- Recruitment: Post job vacancies, upload CVs, track applications
- Dashboard: Validate widgets, quick links, summary data
- Exploratory: Random navigation, UI edge cases, filter stress tests

## Platforms & Tools
- Browsers: Chrome (latest), Edge (latest)
- Devices: Desktop only
- Tools: Git & GitHub, Excel/Google Sheets, VS Code/Notepad++, Lightshot/Snagit

## Project Structure
/OrangeHRMTesting  
│  
├── TestPlan/  
│   └── OrangeHRM_Test_Plan.md  
├── TestCases/  
│   └── OrangeHRM_TC.xlsx  
├── TestData/  
│   ├── employees.csv  
│   └── profile_pics/  
├── ExecutionResults/  
│   └── Module_Results_Admin.md (and others)  
├── Reports/  
│   ├── Daily_Report_YYYY-MM-DD.md  
│   └── Final_Report.md  
└── README.md  

## Test Case Suite
- Total 50 test cases covering:
  - Admin (12)
  - PIM (12)
  - Leave (8)
  - Recruitment (8)
  - Dashboard (5)
  - Exploratory (5)

## Work Plan Summary
- **Day 1:** Setup & initial test cases for Admin and PIM  
- **Day 2:** Finalize test cases and test data  
- **Day 3:** Execute Admin & PIM tests, log bugs  
- **Day 4:** Execute Leave & Recruitment, log bugs, daily reporting  
- **Day 5:** Dashboard & exploratory testing, retesting  
- **Day 6:** Final reporting, issue cleanup, prepare portfolio materials  

## How to Use
1. Clone this repository.
2. Review test plans and test cases.
3. Execute tests on Chrome and Edge browsers.
4. Document results and file bugs on GitHub Issues.
5. Review daily and final reports for insights.

---

*This project is part of a manual testing course to practice functional testing and defect tracking on a real HR system.*
