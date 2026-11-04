# OrangeHRM Test Scenarios

This document defines the high-level test scenarios for the Login, PIM /
Employee Management, and Leave Management modules. Detailed steps, test data,
expected results, and execution statuses will be documented during test-case
creation.

## 1. Login and Session Management

| Scenario ID | Test Scenario | Coverage |
|---|---|---|
| LOGIN-S01 | Verify login with valid credentials | Confirm that an authorized user can log in successfully. |
| LOGIN-S02 | Verify login with an invalid username | Confirm that access is denied and an appropriate error is displayed. |
| LOGIN-S03 | Verify login with an invalid password | Confirm that access is denied and an appropriate error is displayed. |
| LOGIN-S04 | Verify login with both invalid credentials | Confirm that access is denied when both credentials are incorrect. |
| LOGIN-S05 | Verify login with empty credentials | Confirm that the form handles submission without credentials. |
| LOGIN-S06 | Verify username required-field validation | Confirm that the username field displays validation when left empty. |
| LOGIN-S07 | Verify password required-field validation | Confirm that the password field displays validation when left empty. |
| LOGIN-S08 | Verify password field masking | Confirm that entered password characters are not displayed as plain text. |
| LOGIN-S09 | Verify logout | Confirm that an authenticated user can log out successfully. |
| LOGIN-S10 | Verify access behavior after logout | Confirm that protected pages cannot be accessed through the logged-out session. |

## 2. PIM / Employee Management

| Scenario ID | Test Scenario | Coverage |
|---|---|---|
| PIM-S01 | Verify access to the employee list | Confirm that the user can open and view the employee list. |
| PIM-S02 | Verify employee list display | Confirm that employee records and relevant columns display correctly. |
| PIM-S03 | Search for an employee by valid data | Confirm that a matching employee record can be found. |
| PIM-S04 | Search for an employee with invalid data | Confirm that the system handles a search with no matching records. |
| PIM-S05 | Apply employee-list filters | Confirm that available filters return appropriate employee records. |
| PIM-S06 | Reset employee-list filters | Confirm that search and filter criteria can be cleared. |
| PIM-S07 | Add an employee with valid data | Confirm that a new employee can be added successfully when permitted. |
| PIM-S08 | Add an employee with missing mandatory data | Confirm that required fields prevent incomplete employee creation. |
| PIM-S09 | Add an employee with invalid data | Confirm that invalid input is rejected or validated appropriately. |
| PIM-S10 | Verify employee identifier behavior | Confirm that employee identifiers are handled correctly during creation or editing. |
| PIM-S11 | Edit employee information with valid data | Confirm that existing employee information can be updated. |
| PIM-S12 | Edit employee information with invalid data | Confirm that invalid updates are prevented or validated. |
| PIM-S13 | Delete an employee where permitted | Confirm that an employee record can be deleted when allowed by the demo account. |
| PIM-S14 | Cancel an employee create, edit, or delete action | Confirm that cancel actions do not save unintended changes. |
| PIM-S15 | Verify employee data persistence | Confirm that saved employee changes remain available after navigation or refresh. |

## 3. Leave Management

| Scenario ID | Test Scenario | Coverage |
|---|---|---|
| LEAVE-S01 | Verify access to leave pages | Confirm that the user can open the available leave-management pages. |
| LEAVE-S02 | View leave records | Confirm that leave records and relevant information display correctly. |
| LEAVE-S03 | Search leave records with valid criteria | Confirm that matching leave records can be found. |
| LEAVE-S04 | Search leave records with invalid criteria | Confirm that the system handles a search with no matching records. |
| LEAVE-S05 | Apply available leave filters | Confirm that leave filters return appropriate records. |
| LEAVE-S06 | Reset leave filters | Confirm that selected leave search and filter criteria can be cleared. |
| LEAVE-S07 | Submit a leave request with valid data where permitted | Confirm that a valid leave request can be submitted when the workflow is available. |
| LEAVE-S08 | Submit a leave request with missing mandatory data | Confirm that required fields prevent incomplete submission. |
| LEAVE-S09 | Submit a leave request with invalid data | Confirm that invalid leave input is rejected or validated appropriately. |
| LEAVE-S10 | Verify leave date validation | Confirm that date fields and date relationships are validated. |
| LEAVE-S11 | Verify leave status or workflow behavior | Confirm that available leave statuses and actions behave as expected for the demo user. |
| LEAVE-S12 | Cancel a leave action | Confirm that canceling a leave form or action does not save unintended changes. |
| LEAVE-S13 | Verify leave data persistence | Confirm that saved leave information remains available after navigation or refresh. |

## 4. Cross-Module and Regression Scenarios

| Scenario ID | Test Scenario | Coverage |
|---|---|---|
| REG-S01 | Verify navigation between in-scope modules | Confirm that the user can move between Login, PIM, and Leave without unexpected errors. |
| REG-S02 | Verify session behavior while using in-scope modules | Confirm that authenticated access remains consistent during normal navigation. |
| REG-S03 | Verify recently changed workflows after defect fixes | Confirm that a fix does not break related functionality. |
| REG-S04 | Verify representative critical workflows after major test execution | Confirm that core login, employee, and leave workflows remain functional. |

## 5. Scenario Execution Notes

- These scenarios are high-level coverage items, not detailed test cases.
- Detailed test cases will define preconditions, steps, test data, expected
  results, actual results, status, severity, priority, and evidence.
- Scenarios will be marked as not applicable if the demo account does not
  provide the required permission or workflow.
- No defect or execution result is recorded in this document before manual
  testing is performed.
