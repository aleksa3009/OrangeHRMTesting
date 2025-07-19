# TestData

This folder contains test data used for functional testing of the OrangeHRM Live demo portal.

## Contents

- `employees.csv`  
  Contains mock employee records used for testing the PIM (Personnel Information Management) module. Each row includes:
  - First Name  
  - Last Name  
  - Employee ID  
  - Job Title  
  - Location  
  - ProfilePic (filename)

- `profile_pics/`  
  A collection of sample profile pictures used during employee creation and update workflows.

## Purpose

These files support data-driven test scenarios, particularly for:
- Adding and editing employee records
- Uploading and validating profile pictures
- Validating bulk operations via CSV import

## Notes

All profile pictures were generated using [thispersondoesnotexist.com](https://thispersondoesnotexist.com),  
which creates AI-generated images of non-existent people.  
This ensures full compliance with data privacy and ethical testing standards.
