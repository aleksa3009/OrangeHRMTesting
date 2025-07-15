# Exploratory Testing Report – 15-07-2025 (Day 4)

## Objective:
Exploratory testing session focusing on edge cases, UI boundaries, invalid inputs, overlapping leave requests, and unusual user flows across OrangeHRM modules.

---

### 1. Leave Overlap Edge Case  
**Area:** Leave → Apply Leave  
**Approach:** Applied for leave that partially overlaps with existing approved leave (e.g., existing: July 20–22, test case: July 22–24).  
**Observation:** Application correctly blocked with warning message: "Overlap with existing leave request."  
**Status:** Pass – System handled overlap scenario as expected.

---

### 2. Invalid File Upload  
**Area:** PIM → Add Employee → Upload Picture  
**Approach:** Attempted to upload `.exe` and `.txt` files as profile pictures.  
**Observation:** Both file types rejected; system displayed clear error message “Unsupported file type.”  
**Status:** Pass – Invalid file formats handled appropriately.

---

### 3. UI Boundary – Long Employee Name  
**Area:** PIM → Add Employee  
**Approach:** Entered First Name with 255 characters.  
**Observation:** Name accepted; layout preserved in both Employee List and profile page.  
**Status:** Pass – UI handled long input gracefully without breaking.

---

### 4. Invalid Input – Special Characters in Username  
**Area:** Admin → Add User  
**Approach:** Entered username with special characters (e.g., `admin!@#`).  
**Observation:** Input accepted; on Save, system displayed inline message: “Username cannot contain special characters.”  
**Status:** Pass – Validation triggered correctly at submission.

---

### 5. UI Edge – Rapid Pagination  
**Area:** PIM → Employee List  
**Approach:** Rapidly clicked pagination controls (Next/Previous) to simulate heavy user navigation.  
**Observation:** Pages switched smoothly; no flicker or data loss observed.  
**Status:** Pass – Pagination handled under stress without issues.

---

### 6. Leave – Cancel Button Workflow  
**Area:** Leave → Apply Leave  
**Approach:** Filled part of the form, then clicked “Cancel.”  
**Observation:** Form closed instantly without warning, as designed. No data was saved.  
**Status:** Pass – Cancel functionality behaved as expected.

---

## Summary:
- Total Exploratory Sessions: 6  
- Issues Found: 0  
- System behaved as expected under edge conditions  
- No functional or UI defects observed  