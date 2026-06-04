# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 2 user stories. The scope is restricted to test plans and execution records mapped to these user stories. Analysis excludes non-unit test activities and unrelated defect categories.

**Total User Stories:** 2

The baseline for this analysis consists of 2 user stories that form the reference for measuring coverage, execution success, and defect quality. The scope is limited to unit test coverage and execution records mapped to these user stories.

## Test Coverage Summary

**Coverage Details:**

| Metric | Count | Description |
|--------|-------|-------------|
| Fully Covered | 0 | User stories where all acceptance criteria are Fully Covered |
| Partially Covered | 2 | User stories containing one or more Partially Covered acceptance criteria |
| Not Covered | 0 | User stories where all acceptance criteria are Not Covered |

**Coverage Gap Details:**

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---------------|-------|-------------------|-----------------|
| ORM-001 | AC4 | No testcase explicitly validates approval timestamp capture. | Partially Covered |
| ORM-001 | AC5 | No testcase explicitly validates the $1000 threshold for high-value refunds. | Partially Covered |
| SCM-002 | AC2 | No testcase explicitly validates that resume date is included in the notification. | Partially Covered |
| SCM-002 | AC3 | No testcase explicitly validates that customers can view the scheduled resume date in the portal. | Partially Covered |
| SCM-002 | AC4 | No testcase explicitly validates that pause start date is captured in the audit log. | Partially Covered |
| SCM-002 | AC4 | No testcase explicitly validates that timestamp is captured in the audit log. | Partially Covered |
| SCM-002 | AC5 | No testcase explicitly validates that approval is required before the pause is activated. | Partially Covered |

**Coverage Score:**

| User Story ID | Coverage Score | Color |
|---------------|----------------|-------|
| ORM-001 | 60.00% | 🔴 Red |
| SCM-002 | 0.00% | 🔴 Red |

## Test Execution Summary

**Overall Test Execution Summary:**

Total Test Cases Executed: 30

Total Test Cases Passed: 25

Total Test Cases Failed: 5

**Test Execution Summary:**

| User Story ID | Total Test Cases | Executed | Passed | Failed |
|---------------|------------------|----------|--------|--------|
| ORM-001 | 15 | 15 | 12 | 3 |
| SCM-002 | 15 | 15 | 13 | 2 |

## Consistency Analysis

**Data Mapping Inconsistency Details:**

No inconsistency details available.

**Consistency Metrics Summary:**

| Metric | Count |
|--------|-------|
| Total Test Cases | 30 |
| Total Test Logs | 30 |
| Missing Test Cases | 0 |
| Missing Test Logs | 0 |
| Consistency Status | Consistent |

## Defect Details

| Defect ID | Test Case ID | User Story ID | Defect Description |
|-----------|--------------|---------------|-------------------|
| DEF-ORM-001 | UT_ORM_005 | ORM-001 | Notification template rendering issue |
| DEF-ORM-002 | UT_ORM_009 | ORM-001 | Status history service timeout |
| DEF-ORM-003 | UT_ORM_015 | ORM-001 | Refund workflow synchronization error |
| DEF-SCM-101 | TP_SCM_012 | SCM-002 | Pause reason not captured consistently |
| DEF-SCM-102 | TP_SCM_015 | SCM-002 | Activation allowed without completed approval |

## Conclusion

Remediation is required as multiple user stories contain coverage gaps and test case failures with identified defects are present.
