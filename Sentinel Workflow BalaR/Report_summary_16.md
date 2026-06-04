# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 2 user stories. The scope is restricted to test plans and execution records mapped to these user stories. Analysis excludes non-unit test activities and unrelated defect categories.

**Total User Stories:** 2

The baseline for this analysis consists of 2 user stories that form the reference for measuring coverage, execution success, and defect quality. The scope is limited to unit test coverage and execution records mapped to these user stories.

## Test Coverage Summary

### Coverage Details

| Metric | Count | Description |
|--------|-------|-------------|
| Fully Covered | 0 | User stories where all acceptance criteria are Fully Covered |
| Partially Covered | 2 | User stories containing one or more Partially Covered acceptance criteria |
| Not Covered | 0 | User stories where all acceptance criteria are Not Covered |

### Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---------------|-------|---------------------|-----------------|
| ORM-001 | AC4 | No testcase explicitly validates approval timestamp capture. | Partially Covered |
| ORM-001 | AC5 | No testcase explicitly validates the $1000 threshold for high-value refunds. | Partially Covered |
| SCM-002 | AC2 | No testcase explicitly validates that resume date is included in the notification. | Partially Covered |
| SCM-002 | AC3 | No testcase explicitly validates that customers can view the scheduled resume date in the portal. | Partially Covered |
| SCM-002 | AC4 | No testcase explicitly validates that pause start date is captured in the audit log. | Partially Covered |
| SCM-002 | AC4 | No testcase explicitly validates that timestamp is captured in the audit log. | Partially Covered |
| SCM-002 | AC5 | No testcase explicitly validates that manager approval is required before the pause is activated. | Partially Covered |

### Coverage Score

| User Story ID | Coverage Score | Color |
|---------------|----------------|-------|
| ORM-001 | 60.00% | 🔴 Red |
| SCM-002 | 0.00% | 🔴 Red |

### Legend

- 🟢 Green (90–100%) → High coverage (meets quality expectations)
- 🟠 Amber (70–89%) → Moderate coverage (requires attention)
- 🔴 Red (<70%) → Low coverage (critical gaps present)

### Coverage Score Analysis

Coverage Score (%) = (Fully Covered Acceptance Criteria for the User Story / Total Acceptance Criteria in the User Story) × 100

**Description:**
Coverage Score measures the extent to which the acceptance criteria of an individual user story are validated by corresponding test cases. It indicates how completely the requirements defined within that user story are covered through testing.

**Components:**
- Covered Acceptance Criteria for the User Story: Number of acceptance criteria within the user story that have at least one mapped test case.
- Total Acceptance Criteria in the User Story: Total number of acceptance criteria defined for that specific user story.

**Calculation Scope:**
Coverage Score must be calculated separately for each user story using only the acceptance criteria belonging to that user story. Acceptance criteria from other user stories must not be included in the calculation.

## Test Execution Summary

### Overall Test Execution Summary

**Total Test Cases Executed:** 30

**Total Test Cases Passed:** 25

**Total Test Cases Failed:** 5

### Test Execution Summary

| User Story ID | Total Test Cases | Executed | Passed | Failed |
|---------------|------------------|----------|--------|--------|
| ORM-001 | 15 | 15 | 12 | 3 |
| SCM-002 | 15 | 15 | 13 | 2 |

## Consistency Analysis

### Data Mapping Inconsistency Details

No data available.

### Consistency Metrics Summary

| Metric | Count |
|--------|-------|
| Total Test Cases | 30 |
| Total Test Logs | 30 |
| Missing Test Cases | 0 |
| Missing Test Logs | 0 |
| Consistency Status | Consistent |

## Defect Details

**Defect Rate:** 16.67%

### Defect Rate Analysis

Defect Rate = (Total Defects / Total Test Cases) × 100

**Description:**
Defect Rate measures the proportion of defects identified during testing relative to the total number of test cases executed. It is a key quality metric used to evaluate system stability and testing effectiveness.

**Components:**
- Total Defects: Total number of defects identified during the test cycle
- Total Test Cases: Total number of test cases executed

### Defect Details

| Defect ID | Test Case ID | User Story ID | Defect Description |
|-----------|--------------|---------------|--------------------|
| DEF-ORM-001 | UT_ORM_005 | ORM-001 | Notification template rendering issue |
| DEF-ORM-002 | UT_ORM_009 | ORM-001 | Status history service timeout |
| DEF-ORM-003 | UT_ORM_015 | ORM-001 | Refund workflow synchronization error |
| DEF-SCM-101 | TP_SCM_012 | SCM-002 | Pause reason not captured consistently |
| DEF-SCM-102 | TP_SCM_015 | SCM-002 | Activation allowed without completed approval |

## Conclusion

The report indicates that remediation is required as test case failures and defects exist in the current test suite. Both user stories show critical coverage gaps and execution failures that must be addressed before progression.
