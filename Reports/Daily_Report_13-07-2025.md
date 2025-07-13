# Daily Report – 13-07-2025 (Day 2)

---

## Activities:
- Finalized **Test Case Suite** in `TestCases/OrangeHRM_TC.xlsx` covering all 6 modules:
  - Admin (12 test cases)
  - PIM (12 test cases)
  - Leave (8 test cases)
  - Recruitment (8 test cases)
  - Dashboard (5 test cases)
  - Exploratory (5 test cases)
- Ensured each test case includes: Test ID, Title, Preconditions, Test Steps, Expected Results, Priority, Type.
- Verified consistent formatting (Markdown and spreadsheet).
- Adjusted hardcoded dates in Leave module to match current/future timeline (e.g., July 2025).
- Completed and reviewed test data in `TestData/employees.csv`:
  - 20 realistic employee records with names, IDs, roles, locations.
  - Associated images stored in `TestData/profile_pics/` (downloaded from [thispersondoesnotexist.com](https://thispersondoesnotexist.com/)).
- Structured all test artifacts inside `/OrangeHRMTesting/` project repository.

---

## Environment:
- **OS:** Ubuntu 22.04 LTS  
- **Browsers:** Chrome (latest), Firefox (latest)  
- **Tools:** VS Code, LibreOffice Calc, Lightshot

---

## Issues:
- No technical blockers.
- Note: LibreOffice Calc does not render images from CSV — image file names are used as references for manual upload during PIM testing.

---

## Next Steps (Day 3):
1. Begin execution of test cases for **Admin** and **PIM** modules (24 total).
2. Document all results in `ExecutionResults/Module_Results_Admin.md` and `Module_Results_PIM.md`.
3. Capture screenshots for failed or visually relevant steps using Lightshot.
4. Prepare daily report for Day 3.

