# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 1 user story.

The baseline for this evaluation is the identified user story: SLV-002.

The scope is restricted to unit test cases, execution records, and defect data mapped directly to this user story.

Included within scope:

- Unit test cases linked to user story SLV-002.
- Test execution results covering executed, not executed, passed, and failed outcomes.
- Defect data directly associated with the mapped unit test cases for this user story.

Excluded from scope:

- Integration tests, system tests, and performance tests.
- User stories not mapped to unit test cases.
- External defect logs or unrelated defect categories.

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
| SLV-002 | AC4 | AC4: Processing Log Given a pipeline execution, when the CDC logic completes, then the number of inserted, updated, and deleted rows must be logged in the monitoring table. | Medium | Partially Covered |

| User Story ID | Coverage Score | Color |
|---|---:|---|
| SLV-002 | 80.00% | 🟠 Amber |

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
| DEF_SLV-002_004 | UT_SLV-002_004 | SLV-002 | NULL | Orphan delete handling failed. Pipeline did not handle a delete event for a non-existent key gracefully, violating AC2. | functional_validation | high | open |
| DEF_SLV-002_011 | UT_SLV-002_011 | SLV-002 | NULL | Watermark was incorrectly updated on pipeline failure. This violates the rule that the watermark should only advance on successful runs, violating AC5. | policy_enforcement | high | open |

## Conclusion

Summary of Findings:

The analysis indicates that 1 user story was reviewed. Coverage distribution shows 0 fully covered, 1 partially covered, and 0 not covered user stories. Results show an overall unit test coverage rate of 80.00%, an execution success rate of 86.67%, and a defect rate of 13.33%.

Final Outcome Statement:

Results show that the overall coverage rate is 80.00%, the overall execution stability is 86.67%, and the recorded defect severity includes high severity defects. Based on the reported coverage score classification, the user story is rated Amber.

Conclusion Statement:

The current unit test suite demonstrates partial coverage and recorded execution failures with open high severity defects. Remediation is required before progression.
