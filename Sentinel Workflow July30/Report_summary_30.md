# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report covers 19 user stories (SCM-001 to SCM-019), 95 acceptance criteria, 283 planned unit test cases, and 280 available unit test execution log entries derived from the uploaded source documents.

Document completeness review identified complete user story, test plan, and test log sets for 18 user stories; SCM-008 includes a user story and inferred test plan/log pair under alternate file naming, while SCM-003, SCM-004, SCM-007, SCM-011, SCM-014, SCM-017, SCM-018, and SCM-019 have 15 planned test cases but only 13 execution results each, resulting in 8 missing test logs overall; no standalone defect log documents were provided, so defect details were derived from execution logs only.

## Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-002 | AC2 | Resume date not explicitly validated by any testcase. | Partially Covered |
| SCM-002 | AC3 | Scheduled resume date not explicitly validated by any testcase. | Partially Covered |
| SCM-002 | AC4 | Pause start date not explicitly validated by any testcase. | Partially Covered |
| SCM-003 | AC3 | Next billing cycle changes not explicitly validated by any testcase. | Partially Covered |
| SCM-003 | AC5 | Boundary scenario ambiguous: plan includes exactly 50% approval, while AC states greater than 50%. Missing executed boundary testcase log. | Partially Covered |
| SCM-004 | AC5 | Boundary scenario ambiguous: plan includes exactly $500 approval, while AC states greater than $500. Missing executed boundary testcase log. | Partially Covered |
| SCM-005 | AC4 | Reminder date and channel used not explicitly validated by any testcase. | Partially Covered |
| SCM-005 | AC5 | High-value positive scenario above $10,000 not explicitly validated; boundary test at exactly $10,000 does not satisfy AC obligation. | Partially Covered |
| SCM-006 | AC4 | Previous plan, downgraded plan, effective date, and timestamp not explicitly validated by any testcase. | Partially Covered |
| SCM-006 | AC5 | Customer retention review not explicitly validated by any testcase. | Partially Covered |
| SCM-007 | AC3 | Billing change summary not explicitly validated by any testcase. | Partially Covered |
| SCM-007 | AC4 | Subscription ID, transfer date, and timestamp not explicitly validated; missing executed log for one audit edge testcase. | Partially Covered |
| SCM-008 | AC5 | Fraud review not explicitly validated; exact 5000 boundary testcase not executed. | Partially Covered |
| SCM-009 | AC2 | Missing executed edge testcase log for international SMS delivery. | Partially Covered |
| SCM-009 | AC5 | Missing executed boundary testcase log for 3rd retry attempt. | Partially Covered |
| SCM-010 | AC4 | Payment method used, renewal amount, and timestamp not explicitly validated by any testcase. | Partially Covered |
| SCM-011 | AC3 | Effective end date not explicitly validated by any testcase. | Partially Covered |
| SCM-011 | AC5 | Finance team review not explicitly validated; missing executed testcase log for review workflow. | Partially Covered |
| SCM-012 | AC4 | Prorated amount and effective date not explicitly validated by any testcase. | Partially Covered |
| SCM-013 | AC3 | License expiration not explicitly validated by any testcase. | Partially Covered |
| SCM-013 | AC5 | Administrator notification not explicitly validated by any testcase. | Partially Covered |
| SCM-014 | AC4 | Approver field not explicitly validated; missing executed log for one related testcase does not close gap. | Partially Covered |
| SCM-015 | AC2 | Specific lead time / number of days before expiration not explicitly validated by any testcase. | Partially Covered |
| SCM-016 | AC3 | Total subscription cost not explicitly validated by any testcase. | Partially Covered |
| SCM-016 | AC5 | Regional regulation exception path not explicitly validated by any testcase. | Partially Covered |
| SCM-017 | AC4 | Old payment method reference not explicitly validated; missing executed log for failed-update audit testcase. | Partially Covered |
| SCM-017 | AC5 | Immediate retry using new payment method not explicitly validated by any testcase. | Partially Covered |
| SCM-018 | AC3 | Outstanding balance not explicitly validated by any testcase. | Partially Covered |
| SCM-018 | AC5 | Defined SLA for access restoration not explicitly validated by any testcase. | Partially Covered |
| SCM-019 | AC2 | 30-day advance timing not explicitly validated by any testcase. | Partially Covered |
| SCM-019 | AC4 | Old price and new price not explicitly validated by any testcase. | Partially Covered |

## Consistency Analysis

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM3_015 | Ambiguous | Test plan maps exactly 50% price increase to approval trigger, while AC5 states approval is required only when increase is greater than 50%. | SCM-003 | AC5 | Medium |
| TP_SCM4_015 | Ambiguous | Test plan maps exactly $500 outstanding balance to finance approval trigger, while AC5 states approval is required only when balance is greater than $500. | SCM-004 | AC5 | Medium |
| TP_SCM5_010 | Partial | Testcase mapped to AC4 validates only customer ID and subscription ID, not reminder date, channel used, or delivery status. | SCM-005 | AC4 | Medium |
| TP_SCM5_013 | Ambiguous | Boundary testcase at exactly $10,000 is mapped to AC5, but AC defines high-value as greater than $10,000; positive above-threshold path is absent. | SCM-005 | AC5 | Medium |
| TP_SCM6_010 | Partial | Testcase mapped to AC4 validates only IDs and does not cover previous plan, downgraded plan, effective date, credit issued, and timestamp completely. | SCM-006 | AC4 | Medium |
| TP_SCM6_013 / TP_SCM6_014 / TP_SCM6_015 | Partial | AC5 mapping covers enterprise downgrade flagging and approval workflow but does not explicitly validate required customer retention review. | SCM-006 | AC5 | Medium |
| TP_SCM7_010 | Partial | Testcase mapped to AC4 validates owner IDs only; subscription ID, transfer date, authorization reference, and timestamp require additional evidence. | SCM-007 | AC4 | Medium |
| TP_SCM10_009 / TP_SCM10_010 | Partial | AC4 mapping validates subscription ID and renewal date only; payment method used, renewal amount, and timestamp are not explicitly covered. | SCM-010 | AC4 | Medium |
| TP_SCM11_012 / TP_SCM11_013 | Partial | AC5 mapping validates prorated refund calculation but does not explicitly validate required finance review workflow. | SCM-011 | AC5 | Medium |
| TP_SCM12_008 / TP_SCM12_009 | Partial | AC4 mapping validates plan names and timestamp only; prorated amount and effective date remain uncovered. | SCM-012 | AC4 | Medium |
| TP_SCM13_011 | Partial | Testcase mapped to AC5 validates blocking at license limit but does not validate administrator notification obligation. | SCM-013 | AC5 | Medium |
| TP_SCM14_008 / TP_SCM14_009 | Partial | AC4 mapping validates subscription ID, amount, reason, and timestamp, but approver field is not explicitly validated. | SCM-014 | AC4 | Medium |
| TP_SCM15_003 / TP_SCM15_004 / TP_SCM15_015 | Partial | AC2 mapping validates reminder content and duplicate prevention, but does not validate the specified lead-time rule for reminder timing. | SCM-015 | AC2 | Medium |
| TP_SCM16_005 / TP_SCM16_006 / TP_SCM16_014 | Partial | AC3 mapping validates active add-ons and individual charges, but total subscription cost is not explicitly validated. | SCM-016 | AC3 | Medium |
| TP_SCM17_010 | Partial | Testcase mapped to AC5 confirms pending retry state exists, but does not validate immediate retry using the newly updated payment method. | SCM-017 | AC5 | High |
| TP_SCM18_009 / TP_SCM18_010 | Partial | AC5 mapping validates payment prerequisite and blocking, but does not validate restoration within defined SLA. | SCM-018 | AC5 | Medium |
| TP_SCM19_003 / TP_SCM19_004 / TP_SCM19_005 | Partial | AC2 mapping validates notification content but not the requirement that it be sent at least 30 days in advance. | SCM-019 | AC2 | Medium |
| TP_SCM19_008 / TP_SCM19_009 | Partial | AC4 mapping validates subscription ID, notification sent date, and timestamp, but old and new price fields are not explicitly validated. | SCM-019 | AC4 | Medium |
| TP_SCM3_014 / TP_SCM3_015 | Missing Test Log | Planned edge/boundary testcases are present in plan but absent from execution log. | SCM-003 | AC1 / AC5 | High |
| TP_SCM4_014 / TP_SCM4_015 | Missing Test Log | Planned edge/boundary testcases are present in plan but absent from execution log. | SCM-004 | AC2 / AC5 | High |
| TP_SCM7_014 / TP_SCM7_015 | Missing Test Log | Planned edge/negative testcases are present in plan but absent from execution log. | SCM-007 | AC4 / AC2 | High |
| TP_SCM11_014 / TP_SCM11_015 | Missing Test Log | Planned edge/negative testcases are present in plan but absent from execution log. | SCM-011 | AC1 / AC3 | High |
| TP_SCM14_014 / TP_SCM14_015 | Missing Test Log | Planned negative/edge testcases are present in plan but absent from execution log. | SCM-014 | AC3 / AC5 | High |
| TP_SCM17_014 / TP_SCM17_015 | Missing Test Log | Planned negative/edge testcases are present in plan but absent from execution log. | SCM-017 | AC1 / AC4 | High |
| TP_SCM18_014 / TP_SCM18_015 | Missing Test Log | Planned edge/positive testcases are present in plan but absent from execution log. | SCM-018 | AC4 / AC1 | High |
| TP_SCM19_014 / TP_SCM19_015 | Missing Test Log | Planned negative/edge testcases are present in plan but absent from execution log. | SCM-019 | AC3 / AC5 | High |

## Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM3_015 | Ambiguous | Test plan maps exactly 50% price increase to approval trigger, while AC5 states approval is required only when increase is greater than 50%. | SCM-003 | AC5 | Medium |
| TP_SCM4_015 | Ambiguous | Test plan maps exactly $500 outstanding balance to finance approval trigger, while AC5 states approval is required only when balance is greater than $500. | SCM-004 | AC5 | Medium |
| TP_SCM5_010 | Partial | Testcase mapped to AC4 validates only customer ID and subscription ID, not reminder date, channel used, or delivery status. | SCM-005 | AC4 | Medium |
| TP_SCM5_013 | Ambiguous | Boundary testcase at exactly $10,000 is mapped to AC5, but AC defines high-value as greater than $10,000; positive above-threshold path is absent. | SCM-005 | AC5 | Medium |
| TP_SCM6_010 | Partial | Testcase mapped to AC4 validates only IDs and does not cover previous plan, downgraded plan, effective date, credit issued, and timestamp completely. | SCM-006 | AC4 | Medium |
| TP_SCM6_013 / TP_SCM6_014 / TP_SCM6_015 | Partial | AC5 mapping covers enterprise downgrade flagging and approval workflow but does not explicitly validate required customer retention review. | SCM-006 | AC5 | Medium |
| TP_SCM7_010 | Partial | Testcase mapped to AC4 validates owner IDs only; subscription ID, transfer date, authorization reference, and timestamp require additional evidence. | SCM-007 | AC4 | Medium |
| TP_SCM10_009 / TP_SCM10_010 | Partial | AC4 mapping validates subscription ID and renewal date only; payment method used, renewal amount, and timestamp are not explicitly covered. | SCM-010 | AC4 | Medium |
| TP_SCM11_012 / TP_SCM11_013 | Partial | AC5 mapping validates prorated refund calculation but does not explicitly validate required finance review workflow. | SCM-011 | AC5 | Medium |
| TP_SCM12_008 / TP_SCM12_009 | Partial | AC4 mapping validates plan names and timestamp only; prorated amount and effective date remain uncovered. | SCM-012 | AC4 | Medium |
| TP_SCM13_011 | Partial | Testcase mapped to AC5 validates blocking at license limit but does not validate administrator notification obligation. | SCM-013 | AC5 | Medium |
| TP_SCM14_008 / TP_SCM14_009 | Partial | AC4 mapping validates subscription ID, amount, reason, and timestamp, but approver field is not explicitly validated. | SCM-014 | AC4 | Medium |
| TP_SCM15_003 / TP_SCM15_004 / TP_SCM15_015 | Partial | AC2 mapping validates reminder content and duplicate prevention, but does not validate the specified lead-time rule for reminder timing. | SCM-015 | AC2 | Medium |
| TP_SCM16_005 / TP_SCM16_006 / TP_SCM16_014 | Partial | AC3 mapping validates active add-ons and individual charges, but total subscription cost is not explicitly validated. | SCM-016 | AC3 | Medium |
| TP_SCM17_010 | Partial | Testcase mapped to AC5 confirms pending retry state exists, but does not validate immediate retry using the newly updated payment method. | SCM-017 | AC5 | High |
| TP_SCM18_009 / TP_SCM18_010 | Partial | AC5 mapping validates payment prerequisite and blocking, but does not validate restoration within defined SLA. | SCM-018 | AC5 | Medium |
| TP_SCM19_003 / TP_SCM19_004 / TP_SCM19_005 | Partial | AC2 mapping validates notification content but not the requirement that it be sent at least 30 days in advance. | SCM-019 | AC2 | Medium |
| TP_SCM19_008 / TP_SCM19_009 | Partial | AC4 mapping validates subscription ID, notification sent date, and timestamp, but old and new price fields are not explicitly validated. | SCM-019 | AC4 | Medium |
| TP_SCM3_014 / TP_SCM3_015 | Missing Test Log | Planned edge/boundary testcases are present in plan but absent from execution log. | SCM-003 | AC1 / AC5 | High |
| TP_SCM4_014 / TP_SCM4_015 | Missing Test Log | Planned edge/boundary testcases are present in plan but absent from execution log. | SCM-004 | AC2 / AC5 | High |
| TP_SCM7_014 / TP_SCM7_015 | Missing Test Log | Planned edge/negative testcases are present in plan but absent from execution log. | SCM-007 | AC4 / AC2 | High |
| TP_SCM11_014 / TP_SCM11_015 | Missing Test Log | Planned edge/negative testcases are present in plan but absent from execution log. | SCM-011 | AC1 / AC3 | High |
| TP_SCM14_014 / TP_SCM14_015 | Missing Test Log | Planned negative/edge testcases are present in plan but absent from execution log. | SCM-014 | AC3 / AC5 | High |
| TP_SCM17_014 / TP_SCM17_015 | Missing Test Log | Planned negative/edge testcases are present in plan but absent from execution log. | SCM-017 | AC1 / AC4 | High |
| TP_SCM18_014 / TP_SCM18_015 | Missing Test Log | Planned edge/positive testcases are present in plan but absent from execution log. | SCM-018 | AC4 / AC1 | High |
| TP_SCM19_014 / TP_SCM19_015 | Missing Test Log | Planned negative/edge testcases are present in plan but absent from execution log. | SCM-019 | AC3 / AC5 | High |

## Consistency Metrics Summary

| Metric | Count |
|---|---|
| total_testcases | 283.00 |
| total_testlogs | 275.00 |
| missing_testcases | 0.00 |
| missing_testlogs | 8.00 |
| consistency_status | Partially Consistent |

## Defect Details

| Defect ID | Test Case ID | User Story ID | Defect Title | Defect Description |
|---|---|---|---|---|
| DEF-SCM1-001 | UT_SCM1_005 | SCM-001 | Notification template rendering issue | Notification template rendering issue |
| DEF-SCM1-002 | UT_SCM1_009 | SCM-001 | Refund workflow synchronization error | Refund workflow synchronization error |
| DEF-SCM2-101 | TP_SCM2_008 | SCM-002 | Pause reason not captured consistently | Pause reason not captured consistently |
| DEF-SCM2-102 | TP_SCM2_009 | SCM-002 | Activation allowed without completed approval | Activation allowed without completed approval |
| DEF-SCM3-101 | TP_SCM3_004 | SCM-003 | Revised billing amount not included in upgrade confirmation notification | Revised billing amount not included in upgrade confirmation notification |
| DEF-SCM3-102 | TP_SCM3_009 | SCM-003 | Manager approval workflow not initiated when price increase equals exactly 50% | Manager approval workflow not initiated when price increase equals exactly 50% |
| DEF-SCM4-101 | TP_SCM4_004 | SCM-004 | Applicable refund details not included in cancellation confirmation notification | Applicable refund details not included in cancellation confirmation notification |
| DEF-SCM4-102 | TP_SCM4_009 | SCM-004 | Finance team approval workflow fails for mixed currency outstanding balances | Finance team approval workflow fails for mixed currency outstanding balances |
| DEF-SCM5-101 | TP_SCM5_005 | SCM-005 | Renewal amount not populated in 30-day reminder notification for monthly billing plans | Renewal amount not populated in 30-day reminder notification for monthly billing plans |
| DEF-SCM5-103 | TP_SCM5_011 | SCM-005 | System sends reminder even when subscription expiry date is null | System sends reminder even when subscription expiry date is null |
| DEF-SCM5-104 | TP_SCM5_013 | SCM-005 | Boundary condition error: $10,000 subscription flagged as high-value instead of requiring value >$10,000 | Boundary condition error: $10,000 subscription flagged as high-value instead of requiring value >$10,000 |
| DEF-SCM5-105 | TP_SCM5_015 | SCM-005 | Reminder log delivery status remains blank when notification channel fails | Reminder log delivery status remains blank when notification channel fails |
| DEF-SCM6-101 | TP_SCM6_005 | SCM-006 | Adjusted billing amount not included in downgrade confirmation notification to customer | Adjusted billing amount not included in downgrade confirmation notification to customer |
| DEF-SCM6-102 | TP_SCM6_012 | SCM-006 | Audit log not created when downgrade results in zero credit amount | Audit log not created when downgrade results in zero credit amount |
| DEF-SCM6-103 | TP_SCM6_015 | SCM-006 | Enterprise downgrade not held pending state; processed immediately bypassing approval workflow | Enterprise downgrade not held pending state; processed immediately bypassing approval workflow |
| DEF-SCM7-101 | TP_SCM7_005 | SCM-007 | New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint | New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint |
| DEF-SCM7-102 | TP_SCM7_012 | SCM-007 | Compliance approval workflow not initiated for transfers involving tax jurisdiction change only without entity change | Compliance approval workflow not initiated for transfers involving tax jurisdiction change only without entity change |
| DEF-SCM7-103 | TP_SCM7_014 | SCM-007 | Audit log authorization reference field empty when transfer initiated via bulk admin API | Audit log authorization reference field empty when transfer initiated via bulk admin API |
| DEF-SCM8-001 | UT_SCM8_003 | SCM-008 | Points posting service delay | Points posting service delay |
| DEF-SCM8-002 | UT_SCM8_007 | SCM-008 | Balance refresh cache issue | Balance refresh cache issue |
| DEF-SCM8-003 | UT_SCM8_009 | SCM-008 | Redemption workflow synchronization issue | Redemption workflow synchronization issue |
| DEF-SCM9-001 | UT_SCM9_004 | SCM-009 | SMS gateway timeout prevents delivery | SMS gateway timeout prevents delivery |
| DEF-SCM9-002 | UT_SCM9_012 | SCM-009 | Push notification service ignores user preference flag | Push notification service ignores user preference flag |
| DEF-SCM10-101 | TP_SCM10_005 | SCM-010 | Reminder notification omits current plan price for annual-billed subscriptions | Reminder notification omits current plan price for annual-billed subscriptions |
| DEF-SCM10-102 | TP_SCM10_012 | SCM-010 | Subscription remains active state after 3rd failed retry instead of moving to suspended | Subscription remains active state after 3rd failed retry instead of moving to suspended |
| DEF-SCM11-101 | TP_SCM11_013 | SCM-011 | Prorated refund calculation returns small negative value for last-day-of-cycle cancellations | Prorated refund calculation returns small negative value for last-day-of-cycle cancellations |
| DEF-SCM11-102 | TP_SCM11_014 | SCM-011 | Duplicate cancellation request accepted when subscription already pending cancellation | Duplicate cancellation request accepted when subscription already pending cancellation |
| DEF-SCM12-101 | TP_SCM12_014 | SCM-012 | Feature access delayed by several minutes for upgrades processed at midnight billing boundary | Feature access delayed by several minutes for upgrades processed at midnight billing boundary |
| DEF-SCM12-102 | TP_SCM12_015 | SCM-012 | Prorated charge incorrectly applied at full price when upgrade occurs on last day of billing cycle | Prorated charge incorrectly applied at full price when upgrade occurs on last day of billing cycle |
| DEF-SCM13-101 | TP_SCM13_005 | SCM-013 | Revoking license from team member with no assignment returns generic server error instead of handled message | Revoking license from team member with no assignment returns generic server error instead of handled message |
| DEF-SCM13-102 | TP_SCM13_012 | SCM-013 | License pool count briefly shows incorrect total when revoke and reassign occur within same second | License pool count briefly shows incorrect total when revoke and reassign occur within same second |
| DEF-SCM14-101 | TP_SCM14_009 | SCM-014 | Refund reason field truncated to 50 characters in audit log for long free-text reasons | Refund reason field truncated to 50 characters in audit log for long free-text reasons |
| DEF-SCM14-102 | TP_SCM14_013 | SCM-014 | Refund request above threshold processed automatically before finance manager approval recorded | Refund request above threshold processed automatically before finance manager approval recorded |
| DEF-SCM15-101 | TP_SCM15_013 | SCM-015 | Conversion attempted using expired payment method instead of failing over to downgrade path | Conversion attempted using expired payment method instead of failing over to downgrade path |
| DEF-SCM15-102 | TP_SCM15_014 | SCM-015 | Downgrade notification not sent when conversion fails due to invalid (vs missing) payment method | Downgrade notification not sent when conversion fails due to invalid (vs missing) payment method |
| DEF-SCM16-101 | TP_SCM16_013 | SCM-016 | Prorated charge for add-on added on last day of billing cycle rounds up to full month charge | Prorated charge for add-on added on last day of billing cycle rounds up to full month charge |
| DEF-SCM16-102 | TP_SCM16_015 | SCM-016 | Audit log merges two rapid add-on actions into a single entry, losing the first action | Audit log merges two rapid add-on actions into a single entry, losing the first action |
| DEF-SCM17-101 | TP_SCM17_012 | SCM-017 | International card format with alphanumeric routing details rejected as invalid | International card format with alphanumeric routing details rejected as invalid |
| DEF-SCM17-102 | TP_SCM17_015 | SCM-017 | No audit log entry created when payment method update fails midway through processing | No audit log entry created when payment method update fails midway through processing |
| DEF-SCM18-101 | TP_SCM18_011 | SCM-018 | Consecutive failure counter does not reset after an intervening successful payment | Consecutive failure counter does not reset after an intervening successful payment |
| DEF-SCM18-102 | TP_SCM18_014 | SCM-018 | Suspension audit log omits failed attempts that occurred in a prior billing cycle | Suspension audit log omits failed attempts that occurred in a prior billing cycle |
| DEF-SCM19-101 | TP_SCM19_012 | SCM-019 | Only one of several simultaneous tier price changes is detected and flagged for notification | Only one of several simultaneous tier price changes is detected and flagged for notification |
| DEF-SCM19-102 | TP_SCM19_015 | SCM-019 | Downgrade request submitted on effective date boundary is charged a penalty fee in error | Downgrade request submitted on effective date boundary is charged a penalty fee in error |

## Conclusion

Unit test coverage is broadly established across all 19 user stories, but overall quality is only partially compliant due to 8 missing execution logs, multiple partially covered acceptance criteria, ambiguous boundary mappings, and 42 logged defects derived from execution evidence. Remediation is required to execute missing planned tests, close explicit requirement-field coverage gaps, correct mapping ambiguities, and resolve open defects before the suite can be considered audit-ready.
