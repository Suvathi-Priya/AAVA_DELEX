# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 1 user story.

The baseline for this evaluation is the identified user story: STG-001.

The scope is restricted to unit test cases, execution records, and defect data mapped directly to this user story.

Included in scope:
- Unit test cases linked to STG-001.
- Test execution results covering executed, not executed, passed, and failed outcomes.
- Defect records directly associated with STG-001.

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
| STG-001 | AC1 | Zone Creation: Given a new Data Lake account, when initialized, then separate root containers for /bronze, /silver, and /gold must be created. | Medium | Partially Covered |
| STG-001 | AC2 | Domain Organization: Given the /bronze container, when data is ingested, then it must be organized by domain folders (e.g., /sales, /finance). | Medium | Partially Covered |
| STG-001 | AC3 | Tiered Storage Policy: Given files in the /bronze layer, when they exceed 90 days of age, then they must automatically move to Cool storage via lifecycle policy. | Medium | Partially Covered |
| STG-001 | AC4 | Encryption Validation: Given data landing in any zone, when stored at rest, then it must be encrypted using Microsoft-managed and Customer-managed keys. | Critical | Partially Covered |

| User Story ID | Coverage Score | Color |
|---|---:|---|
| STG-001 | 60.00% | 🔴 Red |

Legend:

🟢 Green (90–100%) → High coverage (meets quality expectations)  
🟠 Amber (70–89%) → Moderate coverage (requires attention)  
🔴 Red (<70%) → Low coverage (critical gaps present)

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
| STG-001 | 15 | 15 | 0 | 13 | 2 | 100.00% | 86.67% |

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
| DEF_STG-001_004 | UT_STG-001_004 | STG-001 | NULL | Ingestion Failure for New Domain. Functionality Check: Auto-creation of missing domain folder or rejection of ingestion. Actual Behavior: The system failed to correctly handle ingestion when the target domain folder in /bronze did not exist, violating AC2. | functional_validation | medium | open |
| DEF_STG-001_011 | UT_STG-001_011 | STG-001 | NULL | ACL Policy Bypass. Functionality Check: Deny access to /gold container for user with only /bronze access. Actual Behavior: The user with only /bronze access was not denied access to the /gold container, indicating a failure in ACL enforcement, violating AC5. | policy_enforcement | high | open |

## Conclusion

Summary of Findings:

A total of 1 user story was reviewed. Coverage distribution shows 0 fully covered, 1 partially covered, and 0 not covered user stories. Execution success rate is 86.67%, and defect rate is 13.33%.

Final Outcome Statement:

The overall coverage rate is 60.00%, the overall execution stability is 86.70%, and the recorded defect severity includes medium and high defects. Based on the reported coverage score classification, the current result aligns with Red coverage status.

Conclusion Statement:

The current unit test suite is not sufficient to proceed without remediation. Coverage gaps and open defects require correction before progression.
