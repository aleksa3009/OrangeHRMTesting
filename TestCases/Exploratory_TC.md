# OrangeHRM Manual Testing – Test Cases

## Exploratory Module – 5 Test Cases

### Exploratory_TC_01  
**Title:** Verify navigation through top bar tabs does not break layout  

**Preconditions:**  
- Logged in as Admin  

**Test Steps & Expected Results:**  
1. Click all top navigation tabs rapidly.  
   - *Expected Result:* Pages load correctly; no layout breakage.  

**Priority:** Medium  
**Type:** Exploratory  

---

### Exploratory_TC_02  
**Title:** Verify handling of invalid filter input  

**Preconditions:**  
- On Employee List page  

**Test Steps & Expected Results:**  
1. Enter invalid characters in name search.  
   - *Expected Result:* No crash; shows “No records found”.  

**Priority:** Medium  
**Type:** Negative Functional  

---

### Exploratory_TC_03  
**Title:** Verify long input in search filters does not break UI  

**Preconditions:**  
- On Admin → User Management page  

**Test Steps & Expected Results:**  
1. Paste 255-character string into Username field.  
   - *Expected Result:* Field accepts input; no UI distortion, horizontal scroll, or element overlap occurs.  

**Priority:** Medium  
**Type:** UI  

---

### Exploratory_TC_04  
**Title:** Verify combo filters return correct result  

**Preconditions:**  
- On Employee List page  

**Test Steps & Expected Results:**  
1. Select Job Title = “QA Engineer” and Sub Unit = “IT”.  
   - *Expected Result:* Filter returns employees matching both conditions.  

**Priority:** Medium  
**Type:** Functional  

---

### Exploratory_TC_05  
**Title:** Verify app behavior when session times out  

**Preconditions:**  
- Logged in and idle for 30+ minutes  

**Test Steps & Expected Results:**  
1. Try to perform any action after timeout.  
   - *Expected Result:* Redirected to login page with “Your session has expired” message; user must re-authenticate.  

**Priority:** Medium  
**Type:** Exploratory 