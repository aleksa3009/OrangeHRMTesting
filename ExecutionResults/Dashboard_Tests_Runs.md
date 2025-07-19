# Execution Results – Dashboard Module  
**Date:** 14-07-2025  
**Tester:** Aleksa Aleksić 
**Module:** Admin  
**Browser:** Chrome 138.0.7204.100  
**Environment:** Ubuntu 22.04 LTS 

---

### Dashboard_TC_01: Verify Admin sees correct employee distribution widget  
**Start Time:** 13:30  
**End Time:** 13:34  
**Status:** PASS  

**Test Steps & Observations:**  
1. Navigated to Dashboard → “Employee Distribution by Subunit” widget visible.  
2. Hovered over chart → Tooltip with subunit name and count appeared.

---

### Dashboard_TC_02: Verify Quick Launch links work correctly  
**Start Time:** 13:35  
**End Time:** 13:38  
**Status:** PASS  

**Test Steps & Observations:**  
1. Clicked “Apply Leave” → Navigated to Apply Leave form.  
2. Clicked “My Info” → My Info page opened.

---

### Dashboard_TC_03: Verify Dashboard widgets align properly on all resolutions  
**Start Time:** 13:38  
**End Time:** 13:43  
**Status:** FAIL  

**Test Steps & Observations:**  
1. Opened Dashboard at 1920x1080 → Widgets aligned correctly.  
2. Opened Dashboard at 1366x768 → Widgets overlapped and some overflowed sidebar.  

**Bug:** Layout not responsive on smaller resolutions.

**Screenshot:**

![Screenshot](/ExecutionResults/Screenshots/BUG-012.png)

---

### Dashboard_TC_04: Verify Dashboard updates with real-time data  
**Start Time:** 13:45  
**End Time:** 13:47  
**Status:** PASS  

**Test Steps & Observations:**  
1. Verified “Pending Leave Requests” → Data reflected latest entries.

---

### Dashboard_TC_05: Verify Leave List and Time At Work are visible on Dashboard  
**Start Time:** 13:49  
**End Time:** 13:52  
**Status:** PASS  

**Test Steps & Observations:**  
1. Both “Leave List” and “Time at Work” widgets visible on Dashboard.

---

# Summary
- **Total Test Cases:** 5  
- **Passed:** 4  
- **Failed:** 1  
- **Execution Duration:** 22min (13:30–13:52)

Bug logged for: Responisve layout design error (TC_03).