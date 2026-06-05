# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 1 user stories. The scope is restricted to test plans and execution records mapped to these user stories. Analysis excludes non-unit test activities and unrelated defect categories.

**Coverage Boundary:**
- Total number of user stories included in the analysis: 1
- These user stories form the baseline for evaluation
- Scope is limited to unit test coverage and execution records mapped to these user stories

**Inclusions:**
- Unit test cases linked to the identified user stories
- Test execution results (executed, not executed, passed, failed)
- Defect data directly associated with these user stories

**Exclusions:**
- Integration tests, system tests, or performance tests
- User stories not mapped to test cases

**Baseline Definition:**
The user stories serve as the baseline reference for measuring coverage, execution success, and defect quality.

## Test Coverage Summary

**Total User Stories:** 1

**Coverage Details:**

| Metric | Count | Description |
|--------|-------|-------------|
| Fully Covered | 1 | User stories where all acceptance criteria are Fully Covered |
| Partially Covered | 0 | User stories containing one or more Partially Covered acceptance criteria |
| Not Covered | 0 | User stories where all acceptance criteria are Not Covered |

**Coverage Gap Details:**

No coverage gaps identified as all user stories are fully covered.

**Coverage Score:**

| User Story ID | Coverage Score | Color |
|---------------|----------------|-------|
| SCM-007 | 100.00% | 🟢 Green |

## Test Execution Summary

**Overall Test Execution Summary:**

Total Test Cases Executed: 15

Total Test Cases Passed: 13

Total Test Cases Failed: 2

**Test Execution Summary:**

| User Story ID | Total Test Cases | Executed | Passed | Failed |
|---------------|------------------|----------|--------|--------|
| SCM-007 | 15 | 15 | 13 | 2 |

## Consistency Analysis

**Data Mapping Inconsistency Details:**

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|--------------|------------------|-------------|---------------|-------|--------------|
| TP_SCM7_001 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_001 | SCM-007 | AC1 | High |
| TP_SCM7_002 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_002 | SCM-007 | AC1 | High |
| TP_SCM7_003 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_003 | SCM-007 | AC1 | High |
| TP_SCM7_004 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_004 | SCM-007 | AC2 | High |
| TP_SCM7_005 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_005 | SCM-007 | AC2 | High |
| TP_SCM7_006 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_006 | SCM-007 | AC2 | High |
| TP_SCM7_007 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_007 | SCM-007 | AC3 | High |
| TP_SCM7_008 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_008 | SCM-007 | AC3 | High |
| TP_SCM7_009 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_009 | SCM-007 | AC3 | High |
| TP_SCM7_010 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_010 | SCM-007 | AC4 | High |
| TP_SCM7_011 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_011 | SCM-007 | AC4 | High |
| TP_SCM7_012 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_012 | SCM-007 | AC4 | High |
| TP_SCM7_013 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_013 | SCM-007 | AC5 | High |
| TP_SCM7_014 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_014 | SCM-007 | AC5 | High |
| TP_SCM7_015 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_015 | SCM-007 | AC5 | High |

**Consistency Metrics Summary:**

| Metric | Count |
|--------|-------|
| Total Test Cases | 0 |
| Total Test Logs | 15 |
| Missing Test Cases | 15 |
| Missing Test Logs | 0 |
| Consistency Status | Mismatch Detected |

## Defect Details

**Defect Details:**

| Defect ID | Test Case ID | User Story ID | Defect Description |
|-----------|--------------|---------------|-------------------|
| DEF-SCM7-101 | TP_SCM7_005 | SCM-007 | New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint |
| DEF-SCM7-102 | TP_SCM7_014 | SCM-007 | Compliance approval workflow not initiated for transfers involving tax jurisdiction change only without entity change |

## Conclusion

Remediation is required as test case failures and defects exist in the unit test suite. The report identifies 2 failed test cases and 2 defects that must be addressed before progression.
