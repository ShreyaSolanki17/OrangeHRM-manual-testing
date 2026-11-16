# OrangeHRM Manual Testing Project

## Project Overview

This portfolio project demonstrates a complete manual QA workflow for the
OrangeHRM demo application:

- Test planning and scope definition
- High-level scenario design
- Detailed test-case creation
- Manual test execution and evidence tracking
- Defect investigation and reporting
- Retesting and regression testing
- Test execution summary and project documentation

## Application Under Test

- **Application:** OrangeHRM Demo
- **Modules:** Login, PIM / Employee Management, and Leave Management
- **Environment:** Google Chrome on macOS

## Testing Scope

The project covers:

- Functional and UI testing
- Positive and negative testing
- Required-field and boundary validation
- Login, logout, and session protection
- Employee search, filtering, creation, editing, deletion, and persistence
- Leave search, filtering, validation, submission, cancellation, and status
  workflows
- Focused regression testing of critical workflows

Performance, security, API, database, cross-browser, and cross-device testing
are outside the project scope.

## Test Results

| Metric | Result |
|---|---:|
| Primary test cases | 39 |
| Passed | 38 |
| Failed during initial execution | 1 |
| Blocked | 0 |
| Regression checks passed | 6 |
| Regression checks blocked | 2 |

The initial failed observation involved Leave filter reset behavior. Follow-up
verification cleared the filter successfully, but the available default leave
data returned no records. The behavior is documented as data-dependent and was
not confirmed as a product defect.

## Repository Guide

- [Test Plan](./Test-Plan/OrangeHRM-Test-Plan.md)
- [Test Scenarios](./Test-Plan/OrangeHRM-Test-Scenarios.md)
- [Login Test Cases](./Test-Cases/OrangeHRM-Login-Test-Cases.csv)
- [PIM Test Cases](./Test-Cases/OrangeHRM-PIM-Test-Cases.csv)
- [Leave Test Cases](./Test-Cases/OrangeHRM-Leave-Test-Cases.csv)
- [Test Execution Summary](./Test-Summary/Test-Execution-Summary.md)
- [Regression Results](./Test-Summary/Retesting-and-Regression-Results.md)
- [Leave Filter Investigation](./Bug-Reports/LEAVE-TC06-Reset-Filter.md)

## Tools Used

- OrangeHRM Demo
- Google Chrome
- Chrome DevTools when supporting investigation was useful
- CSV files compatible with Excel or Google Sheets
- Git and GitHub
- Screenshots and execution evidence

## QA Skills Demonstrated

- Test planning and risk identification
- Scenario and test-case design
- Positive, negative, and validation testing
- Test execution and result documentation
- Defect reproduction and evidence-based reporting
- Retesting and regression testing
- Clear technical documentation
