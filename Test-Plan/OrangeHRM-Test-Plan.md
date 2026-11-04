# OrangeHRM Manual Test Plan

## 1. Project Objective

The objective of this project is to evaluate key workflows in the OrangeHRM
demo application through a structured manual testing process. The project will
cover test planning, scenario and test-case design, test execution, evidence
collection, defect reporting, retesting, regression testing, and final
reporting.

## 2. Application Under Test

- **Application:** OrangeHRM Demo
- **Application type:** Web-based human resource management application
- **Primary user role:** Authenticated OrangeHRM demo user
- **Modules in scope:** Login, PIM / Employee Management, and Leave
  Management

## 3. Scope

### 3.1 Features in Scope

#### Login and Session Behavior

- Valid login
- Invalid username and password combinations
- Empty credential submission
- Required-field validation
- Logout
- Access behavior after logout

#### PIM / Employee Management

- Viewing the employee list
- Searching and filtering employees
- Adding an employee
- Mandatory-field validation
- Editing employee information
- Deleting an employee where permitted by the demo account
- Invalid and boundary input validation

#### Leave Management

- Viewing leave-related pages
- Searching and filtering leave records
- Leave form validation
- Valid and invalid input handling
- Available leave status and workflow behavior for the demo user

### 3.2 Features Out of Scope

- Modules outside Login, PIM, and Leave
- Performance, load, and stress testing
- Security penetration testing
- API and database testing
- Cross-browser and cross-device certification
- Production data and production integrations
- Defects in third-party services outside OrangeHRM

The scope may be expanded later if the core testing objectives are complete and
additional coverage provides meaningful value.

## 4. Testing Approach

Testing will be performed manually using documented scenarios and detailed
test cases. Expected results will be defined before execution and will not be
changed to match unexpected application behavior.

The testing approach includes:

- Functional testing
- UI testing
- Positive testing
- Negative testing
- Boundary and validation testing where applicable
- Retesting of confirmed defects where possible
- Regression testing of related workflows after changes or major test flows

## 5. Test Environment

The test environment will be recorded with each execution cycle.

- **Application:** OrangeHRM Demo
- **Browser:** Google Chrome
- **Operating system:** macOS
- **Supporting tool:** Chrome DevTools when console, network, or UI
  investigation is useful
- **Test data:** Demo-account data and non-sensitive employee or leave data
  available in the test environment
- **Evidence:** Screenshots for failed tests, important workflows, and
  representative successful executions

Environment details such as application URL, browser version, and execution
date will be recorded in the relevant test-case or execution documentation.

## 6. Entry Criteria

Testing may begin when:

- The OrangeHRM demo application is accessible.
- A valid demo account is available.
- The Login, PIM, and Leave scope is agreed.
- Test scenarios and detailed test cases are prepared for the planned
  execution cycle.
- Required test data and evidence folders are available.

## 7. Exit Criteria

The planned testing cycle may be considered complete when:

- All planned test cases have been executed or explicitly marked Blocked or
  Not Run.
- Actual results and statuses are recorded.
- Evidence is attached for important executions and failed cases.
- Genuine defects are documented with reproducible details.
- Applicable failed cases have been retested.
- Regression cases have been executed for relevant workflows.
- Test metrics and limitations are included in the final test summary.

## 8. Test Deliverables

The project will produce:

- This test plan
- High-level test scenarios
- Detailed test cases and execution results
- Test execution evidence
- Defect reports and a defect summary
- Retesting and regression results
- Final test execution summary
- Updated project README

## 9. Defect Management

Each confirmed defect will be documented with:

- Bug ID
- Clear title
- Module
- Environment
- Preconditions
- Steps to reproduce
- Expected result
- Actual result
- Severity
- Priority
- Evidence
- Status

Only genuine defects discovered during testing will be reported. If the
application behaves as expected, the successful result will be recorded rather
than creating an artificial defect.

## 10. Risks and Limitations

- The demo environment may change without notice.
- Demo data may be reset, incomplete, or shared with other users.
- Some actions may be restricted by the available user role.
- Defects may not be consistently reproducible in a shared demo environment.
- Availability of Jira or other external tools may affect defect workflow
  documentation.
- Manual testing in one browser and operating system does not establish
  complete cross-browser or cross-device compatibility.
- Performance and security characteristics are not assessed by this plan.

## 11. Approval and Change History

| Version | Date | Description |
|---|---|---|
| 1.0 | 2026-11-03 | Initial test plan created |
