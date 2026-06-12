# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 5 user stories. The scope is restricted to test plans and execution records mapped to these user stories.

Analysis excludes non-unit test activities and unrelated defect categories. The baseline for evaluation consists of 75 unit test cases distributed across SCM-001 through SCM-005 user stories, forming the reference for measuring coverage, execution success, and defect quality.

## Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---------------|-------|---------------------|-----------------|
| SCM-001 | AC5 | No testcase explicitly validates fraud review requirement for high-value refunds. | Partially Covered |
| SCM-002 | AC2 | No testcase explicitly validates that resume date is included in pause confirmation notification. | Partially Covered |
| SCM-002 | AC3 | No testcase explicitly validates that scheduled resume date is viewable in the customer portal. | Partially Covered |
| SCM-002 | AC4 | No testcase explicitly validates that pause start date is captured in audit logs. | Partially Covered |
| SCM-002 | AC5 | No testcase explicitly validates that manager approval is required before pause activation. | Partially Covered |
| SCM-003 | AC3 | No testcase explicitly validates that next billing cycle changes are viewable in the customer portal. | Partially Covered |
| SCM-003 | AC5 | No testcase explicitly validates that manager approval is required before upgrade activation. | Partially Covered |
| SCM-004 | AC5 | No testcase explicitly validates that finance team approval is required before cancellation processing. | Partially Covered |
| SCM-005 | AC4 | No testcase explicitly validates that reminder date is captured in renewal reminder logs.; No testcase explicitly validates that channel used is captured in renewal reminder logs. | Partially Covered |
| SCM-005 | AC5 | No testcase explicitly validates that reminders are sent to customers for high-value subscriptions. | Partially Covered |

## Consistency Analysis

### Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---------------|------------------|-------------|----------------|-------|---------------|
| TP_SCM3_014 | missing_testlog | Execution log is missing for testcase ID: TP_SCM3_014 | SCM-003 | NULL | Medium |
| TP_SCM3_015 | missing_testlog | Execution log is missing for testcase ID: TP_SCM3_015 | SCM-003 | NULL | Medium |

### Consistency Metrics Summary

| Metric | Count |
|---------|-------|
| Total Test Cases | 75 |
| Total Test Logs | 73 |
| Missing Test Cases | 0 |
| Missing Test Logs | 2 |
| Consistency Status | Mismatch Detected |

## Defect Details

| Defect ID | Test Case ID | User Story ID | Defect Description |
|-----------|--------------|---------------|-------------------|
| DEF-ORM-001 | UT_SCM1_005 | SCM-001 | Notification template rendering issue |
| DEF-ORM-002 | UT_SCM1_009 | SCM-001 | Refund workflow synchronization error |
| DEF-SCM-101 | TP_SCM_008 | SCM-002 | Pause reason not captured consistently |
| DEF-SCM-102 | TP_SCM_009 | SCM-002 | Activation allowed without completed approval |
| DEF-SCM3-101 | TP_SCM3_004 | SCM-003 | Revised billing amount not included in upgrade confirmation notification |
| DEF-SCM3-102 | TP_SCM3_009 | SCM-003 | Manager approval workflow not initiated when price increase equals exactly 50% |
| DEF-SCM4-101 | TP_SCM4_004 | SCM-004 | Applicable refund details not included in cancellation confirmation notification |
| DEF-SCM4-102 | TP_SCM4_009 | SCM-004 | Finance team approval workflow fails for mixed currency outstanding balances |
| DEF-SCM5-101 | TP_SCM5_005 | SCM-005 | Renewal amount not populated in 30-day reminder notification for monthly billing plans |
| DEF-SCM5-103 | TP_SCM5_011 | SCM-005 | System sends reminder even when subscription expiry date is null |
| DEF-SCM5-104 | TP_SCM5_013 | SCM-005 | Boundary condition error: $10,000 subscription flagged as high-value instead of requiring value >$10,000 |
| DEF-SCM5-105 | TP_SCM5_015 | SCM-005 | Reminder log delivery status remains blank when notification channel fails |

## Conclusion

Remediation is required. The report identifies coverage gaps across multiple user stories and 12 defects requiring resolution before progression.