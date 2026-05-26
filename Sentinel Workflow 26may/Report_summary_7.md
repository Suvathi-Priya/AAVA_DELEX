# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 1 user story.

The baseline for this evaluation is the identified user story: SLV-002.

The scope is restricted to unit test cases, test execution records, and defect data directly mapped to this user story.

Included in scope:
- Unit test cases linked to the identified user story.
- Test execution results covering executed, not executed, passed, and failed outcomes.
- Defect data directly associated with the identified user story.

Excluded from scope:
- Integration tests, system tests, and performance tests.
- User stories not mapped to test cases.
- External or unrelated defect logs.

The user story baseline is used as the reference for measuring coverage, execution success, and defect quality.

## Test Coverage Summary

Total Use Cases: 1

Coverage Details:

| Metric | Count | Description |
|---|---:|---|
| Fully Covered | 0 | User stories where all acceptance criteria are covered by test cases |
| Partially Covered | 1 | User stories containing a mix of covered and uncovered acceptance criteria |
| Not Covered | 0 | User stories where none of the acceptance criteria are covered by test cases |

Coverage Gap Details:

| User Story ID | AC ID | Acceptance Criteria | Impact Level | Coverage Status |
|---|---|---|---|---|
| SLV-002 | AC3 | AC3: Audit Column Updates Given a record update, when the Merge occurs, then the 'UpdateTimestamp' and 'SourceSystem' metadata columns must be refreshed. | Medium | Partially Covered |

Coverage Score:

| User Story ID | Coverage Score | Color |
|---|---|---|
| SLV-002 | 90.00% | 🟢 Green |

Legend:
- 🟢 Green (90–100%) → High coverage (meets quality expectations)
- 🟠 Amber (70–89%) → Moderate coverage (requires attention)
- 🔴 Red (<70%) → Low coverage (critical gaps present)

Coverage Score Analysis:

Coverage % = (Covered Acceptance Criteria / Total Acceptance Criteria) × 100

Description:

Coverage Percentage measures the extent to which acceptance criteria are validated by corresponding test cases. It indicates how completely the defined requirements are covered through testing.

Components:
- Covered Acceptance Criteria: Number of acceptance criteria that have at least one mapped test case
- Total Acceptance Criteria: Total number of acceptance criteria defined across user stories

## Test Execution Summary

Total Test Cases Executed: 15

Total Test Cases Not Executed: 0

Total Test Cases Passed: 13

Total Test Cases Failed: 2

Execution Success Rate: 86.67%

Test Execution Summary Details:

| User Story ID | Total Test Cases | Executed | Not Executed | Passed | Failed | Execution Rate | Pass Rate |
|---|---:|---:|---:|---:|---:|---:|---:|
| SLV-002 | 15 | 15 | 0 | 13 | 2 | 100.00% | 86.67% |

## Defect Details

Defect Rate: 13.33%

Defect Rate Analysis:

Defect Rate = (Total Defects / Total Test Cases) × 100

Description:

Defect Rate measures the proportion of defects identified during testing relative to the total number of test cases executed. It is a key quality metric used to evaluate system stability and testing effectiveness.

Components:
- Total Defects: Total number of defects identified during the test cycle
- Total Test Cases: Total number of test cases executed

Defect Details:

| Defect ID | Test Case ID | User Story ID | Defect Title | Defect Description | Category | Severity | Status |
|---|---|---|---|---|---|---|---|
| DEF_SLV-002_004 | UT_SLV-002_004 | SLV-002 | NULL | Orphan Delete Handling Failure. Expected graceful handling with a warning for a delete event on a non-existent key. Actual behavior caused an error or did not produce the expected warning, violating AC2. | functional_validation | High | open |
| DEF_SLV-002_011 | UT_SLV-002_011 | SLV-002 | NULL | Watermark Update on Failure. The high-watermark was incorrectly updated despite a pipeline failure. Expected watermark to remain unchanged, violating AC5. | data_integrity | Critical | open |

Defect pattern summary:
- Total defects identified: 2.
- Severity distribution includes 1 High defect and 1 Critical defect.
- Affected categories are functional_validation and data_integrity.
- Both defects are in open status.

## Conclusion

Summary of Findings

A total of 1 user story was reviewed. Coverage distribution shows 0 fully covered, 1 partially covered, and 0 not covered user stories. The overall test coverage rate is 90.00%, execution success rate is 86.70%, and defect rate is 13.33%.

Final Outcome Statement

The current result is based on an overall coverage rate of 90.00%, overall execution stability of 86.70%, and open defect severity including High and Critical defects.

Conclusion Statement

The unit test suite is not currently sufficient to proceed without remediation. Coverage is high, but failed executions and open High and Critical defects require resolution before progression.
