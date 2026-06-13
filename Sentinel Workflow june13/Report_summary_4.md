# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 6 user stories. The scope is restricted to test plans and execution records mapped to these user stories. Analysis excludes non-unit test activities and unrelated defect categories. The baseline for evaluation consists of 90 unit test cases distributed across SCM-001 through SCM-006 user stories, forming the reference for measuring coverage, execution success, and defect quality.

## Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---------------|-------|---------------------|-----------------|
| SCM-001 | AC5 | No testcase explicitly validates fraud review requirement for high-value refunds above $1000. | Partially Covered |
| SCM-002 | AC2 | No testcase explicitly validates that resume date is included in pause confirmation notification. | Partially Covered |
| SCM-002 | AC3 | No testcase explicitly validates that scheduled resume date is viewable in the customer portal. | Partially Covered |
| SCM-002 | AC4 | No testcase explicitly validates that pause start date is captured in pause audit logs. | Partially Covered |
| SCM-003 | AC3 | No testcase explicitly validates that next billing cycle changes are viewable in the customer portal. | Partially Covered |
| SCM-005 | AC4 | No testcase explicitly validates that reminder date is captured in renewal reminder logs.; No testcase explicitly validates that channel used is captured in renewal reminder logs. | Partially Covered |
| SCM-005 | AC5 | No testcase explicitly validates that reminders are sent to customer for high-value subscriptions.; No testcase explicitly validates that reminders are sent to assigned account manager for high-value subscriptions. | Partially Covered |
| SCM-006 | AC2 | No testcase explicitly validates that adjusted billing amount is detailed in downgrade confirmation notification. | Partially Covered |
| SCM-006 | AC4 | No testcase explicitly validates that previous plan is captured in downgrade audit logs.; No testcase explicitly validates that downgraded plan is captured in downgrade audit logs.; No testcase explicitly validates that effective date is captured in downgrade audit logs.; No testcase explicitly validates that timestamp is captured in downgrade audit logs. | Partially Covered |
| SCM-006 | AC5 | No testcase explicitly validates that customer retention review is required before enterprise-tier downgrade requests are processed. | Partially Covered |

## Consistency Analysis

### Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|--------------|------------------|-------------|---------------|-------|--------------|
| TP_SCM3_014 | missing_testlog | Execution log is missing for testcase ID: TP_SCM3_014 | SCM-003 | NULL | Medium |
| TP_SCM3_015 | missing_testlog | Execution log is missing for testcase ID: TP_SCM3_015 | SCM-003 | NULL | Medium |

### Consistency Metrics Summary

| Metric | Count |
|--------|-------|
| Total Test Cases | 90 |
| Total Test Logs | 88 |
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
| DEF-SCM6-101 | TP_SCM6_005 | SCM-006 | Adjusted billing amount not included in downgrade confirmation notification to customer |
| DEF-SCM6-102 | TP_SCM6_012 | SCM-006 | Audit log not created when downgrade results in zero credit amount |
| DEF-SCM6-103 | TP_SCM6_015 | SCM-006 | Enterprise downgrade not held pending state; processed immediately bypassing approval workflow |

## Conclusion

Remediation is required before progression. The analysis identifies 10 acceptance criteria with partial coverage gaps and 13 defects across all user stories that require resolution.
