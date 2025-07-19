# Execution Results – Leave Module  
**Date:** 14-07-2025  
**Module:** Leave
**Tester:** Aleksa Aleksić
**Browser:** Chrome 138.0.7204.100  
**Environment:** Ubuntu 22.04 LTS  

---

### Leave_TC_01: Verify user can apply for future leave  
**Start Time:** 11:20  
**End Time:** 11:27  
**Status:** PASS  

**Test Steps & Observations:**  
1. Clicked “Apply” → Form opened correctly.  
2. Selected “From Date” = tomorrow, “To Date” = day after tomorrow → Accepted.  
3. Selected Leave Type “Annual Leave” → Accepted.  
4. Entered remark → Text accepted.  
5. Clicked “Save” → Message “Successfully Saved” appeared; new entry listed.

---

### Leave_TC_02: Verify user cannot apply for past leave  
**Start Time:** 11:28  
**End Time:** 11:33  
**Status:** FAIL  

**Test Steps & Observations:**  
1. Opened Apply form → OK.  
2. Selected “From Date” and “To Date” = 3 days in the past → Picker allowed selection.  
3. Clicked “Save” → Request was submitted **without validation error**.  

**Bug:** Past date validation missing.

**Screenshot:**

![Screenshot](/ExecutionResults/Screenshots/BUG-006.png) 

---

### Leave_TC_03: Verify user cannot apply leave without selecting mandatory fields  
**Start Time:** 11:35  
**End Time:** 11:38  
**Status:** PASS  

**Test Steps & Observations:**  
1. Opened form → OK.  
2. Left From/To Dates blank → Required field warning shown.  
3. Clicked “Save” → Validation messages appeared; form blocked.

---

### Leave_TC_04: Verify overlapping leave request is rejected  
**Start Time:** 11:39  
**End Time:** 11:43  
**Status:** PASS  

**Test Steps & Observations:**  
1. Opened Apply Leave form → OK.  
2. Selected overlapping dates (July 21–23) → Accepted.  
3. Clicked “Save” → Message “You already have a leave request in this period” displayed; submission blocked.

---

### Leave_TC_05: Verify user can cancel an approved leave  
**Start Time:** 11:44  
**End Time:** 11:49  
**Status:** FAIL  

**Test Steps & Observations:**  
1. Opened My Leave list → Approved leave visible.  
2. Clicked “Cancel” → Confirmation appeared.  
3. Confirmed → Status changed to “Cancelled”, message displayed.

**Bug:** Cancellation message is not being displayed.

**Screenshot:**

![Screenshot](/ExecutionResults/Screenshots/BUG-007.png) 

---

### Leave_TC_06: Verify leave balance updates after applying leave  
**Start Time:** 11:50  
**End Time:** 11:56  
**Status:** FAIL  

**Test Steps & Observations:**  
1. Noted balance = 10 days.  
2. Applied 2-day leave → Request submitted.  
3. Refreshed page → **Balance remained 10 days.**  

**Bug:** Leave balance not updated after submission.

**Screenshot:**

![Screenshot](/ExecutionResults/Screenshots/BUG-008.png) 

---

### Leave_TC_07: Verify error message when leave type is not selected  
**Start Time:** 11:58  
**End Time:** 12:02  
**Status:** PASS  

**Test Steps & Observations:**  
1. Selected valid dates.  
2. Left Leave Type empty.  
3. Clicked “Save” → Message “This field is required” shown near Leave Type.

---

### Leave_TC_08: Verify overlap check for partial overlaps  
**Start Time:** 12:03  
**End Time:** 12:06  
**Status:** PASS  

**Test Steps & Observations:**  
1. Selected “From Date” = July 22, “To Date” = July 24.  
2. Clicked “Save” → Warning shown: “Overlap with existing leave request”; submission blocked.

---

# Summary
- **Total Test Cases:** 8  
- **Passed:** 5  
- **Failed:** 3  
- **Execution Duration:** 46min (11:20–12:06)

Bugs logged for: Date validation error (TC_02), cancellation message bug (TC_05) and balance update error (TC_06).