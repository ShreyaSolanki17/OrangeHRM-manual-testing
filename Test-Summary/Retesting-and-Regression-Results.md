# Retesting and Regression Testing Results

## Purpose

This document records focused regression checks performed after completing the
Login, PIM, and Leave test execution. These checks verify that important
workflows remain functional across the tested modules.

## Regression Scope

| Regression ID | Module | Workflow | Expected Result | Actual Result | Status | Evidence |
|---|---|---|---|---|---|---|
| REG-TC01 | Login | Log in with valid credentials | The user is authenticated and the dashboard is displayed. | The user logged in successfully and the dashboard was displayed. | Pass | |
| REG-TC02 | Login | Log out and access a protected page | The user is logged out and protected pages cannot be accessed without authentication. | Logout completed and the protected page redirected to the login page. | Pass | |
| REG-TC03 | PIM | Search for an existing employee | The matching employee record is displayed. | Employee ID 0367 returned one matching record: Ash J Tyson. | Pass | |
| REG-TC04 | PIM | Add an employee with valid data | The employee is saved successfully and can be found in the employee list. | Regression TestUser was saved successfully with Employee ID 2026111402, and the personal-details page opened. | Pass | |
| REG-TC05 | PIM | Edit an employee and verify persistence | The update is saved and remains available after reopening the record. | Employee ID 2026111402 reopened with the updated last name `PersistedUser`. | Pass | |
| REG-TC06 | PIM | Apply a valid employee filter and reset it | Matching records appear, then Reset clears the filter and restores the default list. | Employee ID 0367 returned 1 record. Reset cleared the filters and restored the employee list with 96 records. | Pass | |
| REG-TC07 | Leave | View leave records and status | Available leave records and statuses are displayed correctly. | The authenticated My Leave page returned no records, so leave status behavior could not be verified in this regression run. | Blocked | |
| REG-TC08 | Leave | Apply a leave request where a leave balance is available | A valid request can be submitted successfully. | Blocked: no leave type with available balance was present. | Blocked | |