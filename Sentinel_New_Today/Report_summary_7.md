# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 2 user stories. These user stories form the baseline for evaluation.

The scope is restricted to unit test cases, execution records, and defect data mapped to these user stories. Included in this analysis are unit test cases linked to the identified user stories, test execution results (executed, not executed, passed, failed), and defect data directly associated with these user stories.

Analysis excludes integration tests, system tests, performance tests, user stories not mapped to test cases, and any external or unrelated defect logs.

The user stories are the baseline reference for measuring coverage, execution success, and defect quality.

## Test Coverage Summary

Total Use Cases: 2

Coverage Details:

| Metric | Count | Description |
|---|---:|---|
| Fully Covered | 0 | User stories where all acceptance criteria are covered by test cases |
| Partially Covered | 2 | User stories containing a mix of covered and uncovered acceptance criteria |
| Not Covered | 0 | User stories where none of the acceptance criteria are covered by test cases |

Coverage Gap Details:

| User Story ID | AC ID | Acceptance Criteria | Impact Level | Coverage Status |
|---|---|---|---|---|
| PAY-001 | AC1 | System must process payments for all supported payment methods. | NULL | Partially Covered |
| PAY-001 | AC2 | Failed payment attempts must generate audit logs with user ID and timestamp. | NULL | Partially Covered |
| ORD-001 | AC4 | Partial shipment processing must notify customers. | NULL | Partially Covered |

Coverage Score:

| User Story ID | Coverage Score | Color |
|---|---:|---|
| PAY-001 | 75.00% | 🟠 Amber |
| ORD-001 | 87.50% | 🟠 Amber |

Legend:

Green (90–100%) → High coverage (meets quality expectations)

Amber (70–89%) → Moderate coverage (requires attention)

Red (<70%) → Low coverage (critical gaps present)

Coverage Score Analysis:

Coverage % = (Covered Acceptance Criteria / Total Acceptance Criteria) × 100

Description:

Coverage Percentage measures the extent to which acceptance criteria are validated by corresponding test cases. It indicates how completely the defined requirements are covered through testing.

Components:

Covered Acceptance Criteria: Number of acceptance criteria that have at least one mapped test case

Total Acceptance Criteria: Total number of acceptance criteria defined across user stories

## Test Execution Summary

Total Test Cases Executed: 10

Total Test Cases Passed: 6

Total Test Cases Failed: 3

Execution Success Rate = (Test cases Passed / Test Cases Executed) × 100 = 60.00%

Test Execution Summary Details:

| User Story ID | Total Test Cases | Total Executed | Passed | Failed |
|---|---:|---:|---:|---:|
| PAY-001 | 8 | 5 | 3 | 2 |
| ORD-001 | 8 | 5 | 3 | 1 |

Data Mapping Inconsistency Details:

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| NULL | NULL | NULL | NULL | NULL | NULL |

Consistency Metrics Summary:

| Metric | Count |
|---|---|
| Total Test Cases | 16 |
| Total Test Logs | 16 |
| Missing Test Cases | 0 |
| Missing Test Logs | 0 |
| Extra Test Cases | 0 |
| Extra Test Logs | 0 |
| Consistency Status | Matched |

## Defect Details

Defect Rate: 18.75%

Defect Rate Analysis:

Defect Rate = (Total Defects / Total Test Cases) × 100

Description:

Defect Rate measures the proportion of defects identified during testing relative to the total number of test cases executed. It is a key quality metric used to evaluate system stability and testing effectiveness.

Components:

Total Defects: Total number of defects identified during the test cycle

Total Test Cases: Total number of test cases executed

Defect Details:

| Defect ID | Test Case ID | User Story ID | Defect Title | Defect Description | Severity | Status |
|---|---|---|---|---|---|---|
| DEF_PAY_001 | TC_PAY_002 | PAY-001 | NULL | Incorrect error message displayed for expired/invalid card payment rejection. | low | open |
| DEF_PAY_002 | TC_PAY_004 | PAY-001 | NULL | Timestamp missing in audit log for failed payment attempts. | high | open |
| DEF_ORD_001 | TC_ORD_004 | ORD-001 | NULL | Shipment status missing in shipment log. | high | open |

## Conclusion

Summary of Findings:

A total of 2 user stories were reviewed. Coverage distribution shows 0 fully covered, 2 partially covered, and 0 not covered user stories. The overall test coverage rate is 81.30%, execution success rate is 60.00%, and defect rate is 18.75%.

Final Outcome Statement:

The overall coverage rate is 81.30%, which corresponds to Amber based on the defined scoring rules. Overall execution stability is 60.00%, and the defect profile includes 2 high severity defects and 1 low severity defect.

Conclusion Statement:

The current unit test suite is not sufficient to proceed without remediation. Coverage gaps, a 60.00% execution success rate, and open high severity defects require corrective action before progression.
