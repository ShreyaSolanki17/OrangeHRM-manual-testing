# OrangeHRM Test Execution Summary

## 1. Test Overview

- **Application:** OrangeHRM Demo
- **Modules tested:** Login, PIM / Employee Management, and Leave Management
- **Testing type:** Manual functional, UI, positive, negative, validation,
  boundary, and regression testing
- **Primary execution environment:** Google Chrome on macOS

## 2. Primary Test Execution Results

| Metric | Result |
|---|---:|
| Total test cases | 39 |
| Passed | 38 |
| Failed | 1 |
| Blocked | 0 |
| Not Run | 0 |

### Results by Module

| Module | Total | Passed | Failed | Blocked | Not Run |
|---|---:|---:|---:|---:|---:|
| Login | 10 | 10 | 0 | 0 | 0 |
| PIM / Employee Management | 16 | 16 | 0 | 0 | 0 |
| Leave Management | 13 | 12 | 1 | 0 | 0 |

## 3. Failed Test Case

### LEAVE-TC06 — Reset Leave Filters

The Pending Approval filter returned leave records, but selecting **Reset**
did not clear the filter or restore the default leave list. This behavior
requires further investigation and formal defect reporting if it is
reproducible.

## 4. Regression Results

| Metric | Result |
|---|---:|
| Regression checks | 8 |
| Passed | 6 |
| Blocked | 2 |

The blocked regression checks were related to Leave data availability. The
authenticated My Leave page returned no records during one check, and no
leave type with available balance was present during the other.

Detailed regression results are documented in
[Retesting-and-Regression-Results.md](./Retesting-and-Regression-Results.md).

## 5. Defect Summary

- **Observed failed behaviors:** 1
- **Formal Jira defects:** None recorded in this execution summary
- **Primary observation:** Leave filter reset did not restore the default list
  during execution.

The failed behavior should be reproduced and documented as a defect before
assigning final severity and priority.

## 6. Major Observations

- Login authentication, validation, logout, and protected-page behavior
  worked as expected.
- PIM employee search, filtering, creation, validation, editing, deletion,
  cancellation, and persistence workflows passed.
- Leave request validation, date validation, cancellation, and persistence
  workflows passed when the required leave balance was available.
- Leave data availability varied during testing, affecting regression
  coverage.

## 7. Testing Limitations

- The OrangeHRM demo environment is shared and may change between executions.
- Available employee and leave data may vary.
- Leave regression coverage was limited when records or balances were
  unavailable.
- Testing was performed in one browser and operating system.
- Performance, security, API, database, cross-browser, and cross-device
  testing were outside the project scope.

## 8. Final Conclusion

The primary manual test execution covered all planned Login, PIM, and Leave
test cases. Most tested workflows behaved as expected, with one failed Leave
filter-reset behavior requiring follow-up. Regression testing confirmed that
the critical Login and PIM workflows continued to operate, while two Leave
regression checks remained blocked by changing demo data availability.
