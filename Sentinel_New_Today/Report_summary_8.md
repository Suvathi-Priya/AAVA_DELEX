# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 1 user story.

The baseline for this evaluation is the following user story: LZ-001.

The scope is restricted to unit test cases, unit test execution records, and defect data directly mapped to this user story.

Included in scope:
- Unit test cases linked to the identified user story.
- Test execution results covering executed, not executed, passed, and failed records.
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
| LZ-001 | AC1 | Subscription Separation: Given the landing zone setup, when environments are created, then separate subscriptions must be used for Dev, QA, and Prod. | NULL | Partially Covered |
| LZ-001 | AC2 | Resource Group Alignment: Given a new project onboarding, when resources are deployed, then they must be grouped into Resource Groups based on the environment. | NULL | Partially Covered |
| LZ-001 | AC5 | Cost Center Tagging: Given any resource deployment, when the "Cost Center" tag is missing, then the deployment must fail validation. | NULL | Partially Covered |

| User Story ID | Coverage Score | Color |
|---|---:|---|
| LZ-001 | 70.00% | 🟠 Amber |

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

Total Test Cases Passed: 13

Total Test Cases Failed: 2

Execution Success Rate: 86.67%

Test Execution Summary Details:

| User Story ID | Total Test Cases | Total Executed | Passed | Failed |
|---|---:|---:|---:|---:|
| LZ-001 | 14 | 15 | 13 | 2 |

Data Mapping Inconsistency Details:

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| UT_LZ-001_014 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_LZ-001_014 | LZ-001 | AC2 | High |
| UT_LZ-001_014 | extra_testlog | Extra execution log exists without corresponding testcase definition: UT_LZ-001_014 | LZ-001 | AC2 | Medium |

Consistency Metrics Summary:

| Metric | Count |
|---|---|
| Total Test Cases | 14 |
| Total Test Logs | 15 |
| Missing Test Cases | 1 |
| Missing Test Logs | 0 |
| Extra Test Cases | 0 |
| Extra Test Logs | 1 |
| Consistency Status | Mismatch Detected |

## Defect Details

Defect Rate: 13.33%

Defect Rate Analysis:

Defect Rate = (Total Defects / Total Test Cases) × 100

Description:

Defect Rate measures the proportion of defects identified during testing relative to the total number of test cases executed. It is a key quality metric used to evaluate system stability and testing effectiveness.

Components:
- Total Defects: Total number of defects identified during the test cycle
- Total Test Cases: Total number of test cases executed

| Defect ID | Test Case ID | User Story ID | Defect Title | Defect Description | Severity | Status |
|---|---|---|---|---|---|---|
| DEF_LZ-001_008 | UT_LZ-001_008 | LZ-001 | NULL | Network security policy violation. Functionality Check: 'Verify that a network connection attempt from a Dev environment resource to a Prod resource is blocked by default'. Actual Behavior: Connection was not blocked, violating AC4. | High | open |
| DEF_LZ-001_013 | UT_LZ-001_013 | LZ-001 | NULL | Tagging Policy Bypass. Functionality Check: 'Validate tag enforcement when the Cost Center tag is present but has an empty or null value'. Actual Behavior: Resource was successfully deployed with an empty tag value, violating AC5. | High | open |

## Conclusion

Summary of Findings:

A total of 1 user story was reviewed. Coverage distribution shows 0 fully covered, 1 partially covered, and 0 not covered user stories. The execution success rate is 86.67%, and the defect rate is 13.33%.

Final Outcome Statement:

The overall coverage rate is 70.00%, the overall execution success rate is 86.70%, and the recorded defect severity includes High defects. Based on these reported values, the unit test suite shows partial coverage with open defect presence.

Conclusion Statement:

The current unit test coverage and quality are not sufficient to support progression without remediation. Coverage gaps, mapping inconsistencies, and open High severity defects require resolution before proceeding.
