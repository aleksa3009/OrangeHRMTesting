# OrangeHRM Manual Testing – Test Cases

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
2. Select “From Date” = July 21, 2025 and “To Date” = July 23, 2025.  
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
