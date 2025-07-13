# OrangeHRM Manual Testing – Test Cases

## Dashboard Module – 5 Test Cases

### Dashboard_TC_01  
**Title:** Verify Admin sees correct employee distribution widget  

**Preconditions:**  
- Logged in as Admin  

**Test Steps & Expected Results:**  
1. Go to Dashboard page.  
   - *Expected Result:* “Employee Distribution by Subunit” widget is visible.  
2. Hover over chart.  
   - *Expected Result:* Tooltip with subunit name and count appears.  

**Priority:** Medium  
**Type:** UI  

---

### Dashboard_TC_02  
**Title:** Verify Quick Launch links work correctly  

**Preconditions:**  
- Logged in as Admin 

**Test Steps & Expected Results:**  
1. Click on “Apply Leave” from Quick Launch.  
   - *Expected Result:* Navigates to Apply Leave form.  
2. Click on “My Info”.  
   - *Expected Result:* My Info page opens.  

**Priority:** Medium  
**Type:** Functional  

---

### Dashboard_TC_03  
**Title:** Verify Dashboard widgets align properly on all resolutions  

**Preconditions:**  
- Browser resolution 1920x1080 and 1366x768  

**Test Steps & Expected Results:**  
1. Open Dashboard.  
   - *Expected Result:* Widgets align without overlap or overflow.  

**Priority:** Low  
**Type:** UI  

---

### Dashboard_TC_04  
**Title:** Verify Dashboard updates with real-time data  

**Preconditions:**  
- At least one employee added today  

**Test Steps & Expected Results:**  
1. Go to Dashboard.  
   - *Expected Result:* “Pending Leave Requests” reflects current data.  

**Priority:** Medium  
**Type:** Functional  

---

### Dashboard_TC_05  
**Title:** Verify Leave List and Time At Work are visible on Dashboard  

**Preconditions:**  
- Logged in as any user  

**Test Steps & Expected Results:**  
1. Go to Dashboard.  
   - *Expected Result:* “Leave List” and “Time at Work” widgets are shown.  

**Priority:** Medium  
**Type:** UI  

---
