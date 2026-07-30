<div align="center">

# **UNIT TEST QUALITY & COVERAGE REPORT**

</div>

# Scope

This report covers 5 user stories (SCM-001 to SCM-005), 75 planned unit test cases, and 72 available unit test execution log entries derived directly from the uploaded source documents. Document completeness validation identified all 5 user story documents, all 5 test plan documents, and all 5 test log documents as readable; no separate defect log documents were uploaded, therefore defect details were derived from defect information embedded in the execution logs. Overall scope includes 25 acceptance criteria, with test mapping present for all user stories; however, execution completeness is partially impacted because SCM-003 and SCM-004 each have 2 planned test cases without corresponding execution log entries, resulting in 3.00 missing test logs in total at portfolio level.

## Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-001 | AC5 | Fraud review validation missing; no testcase explicitly validates fraud review component. | Partially Covered |
| SCM-002 | AC2 | Resume date validation missing from testcase mapping; no testcase explicitly verifies resume date in notification. | Partially Covered |
| SCM-002 | AC3 | Scheduled resume date display not explicitly validated by any testcase. | Partially Covered |
| SCM-003 | AC3 | Next billing cycle changes not explicitly validated by any testcase. | Partially Covered |
| SCM-003 | AC5 | Boundary testcase for exactly 50% exists in plan but has no execution log; requirement wording is >50%, but threshold behavior remains execution-incomplete. | Partially Covered |
| SCM-004 | AC5 | Boundary testcase for exactly $500 exists in plan but has no execution log; threshold boundary execution evidence missing. | Partially Covered |
| SCM-005 | AC4 | Reminder date and channel used are not explicitly validated by testcase mapping. | Partially Covered |
| SCM-005 | AC5 | No positive testcase explicitly validates dual-recipient reminder for subscriptions above $10,000; only boundary and below-threshold behavior are covered. | Partially Covered |

# Consistency Analysis

| Test Case ID | User Story ID | AC ID | Consistency Type | Description | Impact Level |
|---|---|---|---|---|---|
| TP_SCM3_014 | SCM-003 | AC1 | Missing Test Log | Planned edge testcase present in test plan but no execution result found in test log. | Medium |
| TP_SCM3_015 | SCM-003 | AC5 | Missing Test Log | Planned boundary testcase present in test plan but no execution result found in test log. | High |
| TP_SCM4_014 | SCM-004 | AC2 | Missing Test Log | Planned edge testcase present in test plan but no execution result found in test log. | Medium |
| TP_SCM4_015 | SCM-004 | AC5 | Missing Test Log | Planned boundary testcase present in test plan but no execution result found in test log. | High |
| SCM-002 / AC2 | SCM-002 | AC2 | Partial Requirement Mapping | AC requires pause start date and resume date in notification, but testcase mapping validates only pause start date and generic notification behavior. | Medium |
| SCM-002 / AC3 | SCM-002 | AC3 | Partial Requirement Mapping | AC requires pause status, pause history, and scheduled resume date, but testcase mapping validates only pause status and history. | Medium |
| SCM-003 / AC3 | SCM-003 | AC3 | Partial Requirement Mapping | AC requires next billing cycle changes visibility, but no testcase explicitly validates this obligation. | Medium |
| SCM-005 / AC4 | SCM-005 | AC4 | Partial Requirement Mapping | AC requires reminder date, channel used, and delivery status; available testcase mapping validates IDs and failed delivery status only. | Medium |
| SCM-005 / AC5 | SCM-005 | AC5 | Partial Requirement Mapping | AC requires reminders to both customer and assigned account manager for high-value subscriptions, but no positive testcase explicitly validates both recipients. | High |
| SCM-001 / AC5 | SCM-001 | AC5 | Partial Requirement Mapping | AC requires manager approval and fraud review; mapped tests validate approval workflow and threshold behavior only. | High |

## Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM3_014 | Missing Test Log | Planned edge testcase present in test plan but no execution result found in test log. | SCM-003 | AC1 | Medium |
| TP_SCM3_015 | Missing Test Log | Planned boundary testcase present in test plan but no execution result found in test log. | SCM-003 | AC5 | High |
| TP_SCM4_014 | Missing Test Log | Planned edge testcase present in test plan but no execution result found in test log. | SCM-004 | AC2 | Medium |
| TP_SCM4_015 | Missing Test Log | Planned boundary testcase present in test plan but no execution result found in test log. | SCM-004 | AC5 | High |
| SCM-002 / AC2 | Partial Requirement Mapping | AC requires pause start date and resume date in notification, but testcase mapping validates only pause start date and generic notification behavior. | SCM-002 | AC2 | Medium |
| SCM-002 / AC3 | Partial Requirement Mapping | AC requires pause status, pause history, and scheduled resume date, but testcase mapping validates only pause status and history. | SCM-002 | AC3 | Medium |
| SCM-003 / AC3 | Partial Requirement Mapping | AC requires next billing cycle changes visibility, but no testcase explicitly validates this obligation. | SCM-003 | AC3 | Medium |
| SCM-005 / AC4 | Partial Requirement Mapping | AC requires reminder date, channel used, and delivery status; available testcase mapping validates IDs and failed delivery status only. | SCM-005 | AC4 | Medium |
| SCM-005 / AC5 | Partial Requirement Mapping | AC requires reminders to both customer and assigned account manager for high-value subscriptions, but no positive testcase explicitly validates both recipients. | SCM-005 | AC5 | High |
| SCM-001 / AC5 | Partial Requirement Mapping | AC requires manager approval and fraud review; mapped tests validate approval workflow and threshold behavior only. | SCM-001 | AC5 | High |

## Consistency Metrics Summary

| Metric | Count |
|---|---|
| Total Test Cases | 75.00 |
| Total Test Logs | 72.00 |
| Missing Test Cases | 0.00 |
| Missing Test Logs | 3.00 |
| Consistency Status | Partially Consistent |

# Defect Details

| User Story ID | AC ID | Defect ID | Test Case ID | Defect Title / Description |
|---|---|---|---|---|
| SCM-001 | AC2 | DEF-SCM1-001 | UT_SCM1_005 | Notification template rendering issue |
| SCM-001 | AC5 | DEF-SCM1-002 | UT_SCM1_009 | Refund workflow synchronization error |
| SCM-002 | AC4 | DEF-SCM2-101 | TP_SCM2_008 | Pause reason not captured consistently |
| SCM-002 | AC5 | DEF-SCM2-102 | TP_SCM2_009 | Activation allowed without completed approval |
| SCM-003 | AC2 | DEF-SCM3-101 | TP_SCM3_004 | Revised billing amount not included in upgrade confirmation notification |
| SCM-003 | AC5 | DEF-SCM3-102 | TP_SCM3_009 | Manager approval workflow not initiated when price increase equals exactly 50% |
| SCM-004 | AC2 | DEF-SCM4-101 | TP_SCM4_004 | Applicable refund details not included in cancellation confirmation notification |
| SCM-004 | AC5 | DEF-SCM4-102 | TP_SCM4_009 | Finance team approval workflow fails for mixed currency outstanding balances |
| SCM-005 | AC2 | DEF-SCM5-101 | TP_SCM5_005 | Renewal amount not populated in 30-day reminder notification for monthly billing plans |
| SCM-005 | AC1 | DEF-SCM5-103 | TP_SCM5_011 | System sends reminder even when subscription expiry date is null |
| SCM-005 | AC5 | DEF-SCM5-104 | TP_SCM5_013 | Boundary condition error: $10,000 subscription flagged as high-value instead of requiring value >$10,000 |
| SCM-005 | AC4 | DEF-SCM5-105 | TP_SCM5_015 | Reminder log delivery status remains blank when notification channel fails |

## Defect Details

| User Story ID | AC ID | Defect ID | Test Case ID | Defect Title / Description |
|---|---|---|---|---|
| SCM-001 | AC2 | DEF-SCM1-001 | UT_SCM1_005 | Notification template rendering issue |
| SCM-001 | AC5 | DEF-SCM1-002 | UT_SCM1_009 | Refund workflow synchronization error |
| SCM-002 | AC4 | DEF-SCM2-101 | TP_SCM2_008 | Pause reason not captured consistently |
| SCM-002 | AC5 | DEF-SCM2-102 | TP_SCM2_009 | Activation allowed without completed approval |
| SCM-003 | AC2 | DEF-SCM3-101 | TP_SCM3_004 | Revised billing amount not included in upgrade confirmation notification |
| SCM-003 | AC5 | DEF-SCM3-102 | TP_SCM3_009 | Manager approval workflow not initiated when price increase equals exactly 50% |
| SCM-004 | AC2 | DEF-SCM4-101 | TP_SCM4_004 | Applicable refund details not included in cancellation confirmation notification |
| SCM-004 | AC5 | DEF-SCM4-102 | TP_SCM4_009 | Finance team approval workflow fails for mixed currency outstanding balances |
| SCM-005 | AC2 | DEF-SCM5-101 | TP_SCM5_005 | Renewal amount not populated in 30-day reminder notification for monthly billing plans |
| SCM-005 | AC1 | DEF-SCM5-103 | TP_SCM5_011 | System sends reminder even when subscription expiry date is null |
| SCM-005 | AC5 | DEF-SCM5-104 | TP_SCM5_013 | Boundary condition error: $10,000 subscription flagged as high-value instead of requiring value >$10,000 |
| SCM-005 | AC4 | DEF-SCM5-105 | TP_SCM5_015 | Reminder log delivery status remains blank when notification channel fails |

# Conclusion

Unit test coverage is broadly established across all uploaded user stories, but the overall quality status is not fully compliant due to 12 reported defects, 3.00 missing execution logs, and multiple partially covered acceptance criteria with unmet requirement obligations. Remediation is required to close missing mappings and executions, add explicit validation for uncovered AC elements, and resolve approval, notification, logging, and boundary-condition defects before the suite can be considered fully consistent and complete.
