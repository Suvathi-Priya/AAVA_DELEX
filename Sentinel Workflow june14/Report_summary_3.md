<div align="center"><strong><span style="font-size:28px;">UNIT TEST QUALITY & COVERAGE REPORT</span></strong></div>

# Scope

This report evaluates unit test coverage and quality across 6 user stories. The scope is restricted to test plans and execution records mapped to these user stories.

Analysis excludes non-unit test activities and unrelated defect categories. The baseline for evaluation consists of 6 user stories with their associated acceptance criteria, forming the foundation for measuring coverage, execution success, and defect quality.

# Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-001 | AC5 | No testcase explicitly validates fraud review requirement. | Partially Covered |
| SCM-002 | AC2 | No testcase explicitly validates resume date inclusion in notification. | Partially Covered |
| SCM-002 | AC3 | No testcase explicitly validates scheduled resume date visibility in portal. | Partially Covered |
| SCM-002 | AC4 | No testcase explicitly validates pause start date capture in audit log. | Partially Covered |
| SCM-003 | AC3 | No testcase explicitly validates next billing cycle changes visibility in portal. | Partially Covered |
| SCM-005 | AC4 | No testcase explicitly validates reminder date capture in reminder log.; No testcase explicitly validates channel used capture in reminder log. | Partially Covered |
| SCM-005 | AC5 | No testcase explicitly validates reminder sent to customer for high-value subscriptions. | Partially Covered |
| SCM-006 | AC2 | No testcase explicitly validates adjusted billing amount inclusion in notification. | Partially Covered |
| SCM-006 | AC4 | No testcase explicitly validates previous plan capture in audit log.; No testcase explicitly validates downgraded plan capture in audit log.; No testcase explicitly validates effective date capture in audit log.; No testcase explicitly validates timestamp capture in audit log. | Partially Covered |
| SCM-006 | AC5 | No testcase explicitly validates customer retention review requirement. | Partially Covered |

# Consistency Analysis

### Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM3_014 | missing_testlog | Execution log is missing for testcase ID: TP_SCM3_014 | SCM-003 | AC1 | Medium |
| TP_SCM3_015 | missing_testlog | Execution log is missing for testcase ID: TP_SCM3_015 | SCM-003 | AC5 | Medium |

### Consistency Metrics Summary

| Metric | Count |
|---|---|
| Total Test Cases | 88 |
| Total Test Logs | 86 |
| Missing Test Cases | 0 |
| Missing Test Logs | 2 |
| Consistency Status | Mismatch Detected |

# Defect Details

| Defect ID | Test Case ID | User Story ID | Defect Description |
|---|---|---|---|
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

# Conclusion

Remediation is required before progression. Multiple user stories have coverage gaps and 15 defects exist across the test suite that require resolution.
