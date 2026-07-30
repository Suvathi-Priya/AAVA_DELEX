# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 7 user stories (SCM-001 to SCM-007).

These user stories form the baseline for evaluation. The scope is restricted to unit test plans, unit test cases, and execution records mapped to these user stories, as provided in the structured JSON input.

### Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-001 | AC2 | UT_SCM1_005 Status Fail; Actual Result: Notification content generation failed; Defect Details & Description: DEF-SCM1-001 - Notification template rendering issue | Partially Covered |
| SCM-001 | AC5 | UT_SCM1_009 Status Fail; Actual Result: High-value refund processing blocked; Defect Details & Description: DEF-SCM1-002 - Refund workflow synchronization error; No mapped testcase explicitly validates fraud review; UT_SCM1_009 Status Fail; Actual Result: High-value refund processing blocked; Defect Details & Description: DEF-SCM1-002 - Refund workflow synchronization error | Partially Covered |
| SCM-002 | AC2 | No mapped testcase explicitly validates resume date inclusion in the confirmation notification | Partially Covered |
| SCM-002 | AC3 | No mapped testcase explicitly validates scheduled resume date visibility in the customer portal | Partially Covered |
| SCM-002 | AC4 | TP_SCM2_008 Status Fail; Actual Result: Pause reason missing in some records; Defect ID & Description: DEF-SCM2-101 - Pause reason not captured consistently; No mapped testcase explicitly validates pause start date capture in the audit log; TP_SCM2_008 Status Fail; Actual Result: Pause reason missing in some records; Defect ID & Description: DEF-SCM2-101 - Pause reason not captured consistently | Partially Covered |
| SCM-002 | AC5 | TP_SCM2_009 Status Fail; Actual Result: Pause activated before approval validation; Defect ID & Description: DEF-SCM2-102 - Activation allowed without completed approval | Partially Covered |
| SCM-003 | AC1 | TP_SCM3_014 has no explicit validation of submission capability; Actual Result not available because no corresponding execution log entry was provided; TP_SCM3_014 has no explicit validation of preferred upgrade date rejection; Actual Result not available because no corresponding execution log entry was provided | Partially Covered |
| SCM-003 | AC2 | TP_SCM3_004 Status Fail; Actual Result: Revised billing amount missing in notification; Defect ID & Description: DEF-SCM3-101 - Revised billing amount not included in upgrade confirmation notification | Partially Covered |
| SCM-003 | AC3 | No mapped testcase explicitly validates next billing cycle changes visibility in the customer portal | Partially Covered |
| SCM-003 | AC5 | TP_SCM3_009 Status Fail; Actual Result: Approval workflow not triggered for borderline 50% cases; Defect ID & Description: DEF-SCM3-102 - Manager approval workflow not initiated when price increase equals exactly 50% | Partially Covered |
| SCM-004 | AC2 | TP_SCM4_004 Status Fail; Actual Result: Refund details missing from cancellation notification; Defect ID & Description: DEF-SCM4-101 - Applicable refund details not included in cancellation confirmation notification | Partially Covered |
| SCM-004 | AC5 | TP_SCM4_009 Status Fail; Actual Result: Finance approval workflow not triggered consistently; Defect ID & Description: DEF-SCM4-102 - Finance team approval workflow fails for mixed currency outstanding balances | Partially Covered |
| SCM-005 | AC1 | TP_SCM5_011 Status Fail; Actual Result: Reminder still triggered despite missing expiry date, no error logged; Defect ID & Description: DEF-SCM5-103 - System sends reminder even when subscription expiry date is null | Partially Covered |
| SCM-005 | AC2 | TP_SCM5_005 Status Fail; Actual Result: Renewal amount missing in 30-day reminder notification; Defect ID & Description: DEF-SCM5-101 - Renewal amount not populated in 30-day reminder notification for monthly billing plans | Partially Covered |
| SCM-005 | AC4 | TP_SCM5_015 Status Fail; Actual Result: Delivery status not updated to Failed when email channel is unavailable; Defect ID & Description: DEF-SCM5-105 - Reminder log delivery status remains blank when notification channel fails; No mapped testcase explicitly validates reminder date capture in the reminder log | Partially Covered |
| SCM-005 | AC5 | No mapped testcase explicitly validates customer reminder for subscriptions flagged as high-value; TP_SCM5_013 Status Fail; Actual Result: Subscription at exactly $10,000 incorrectly flagged as high-value; Defect ID & Description: DEF-SCM5-104 - Boundary condition error: $10,000 subscription flagged as high-value instead of requiring value >$10,000 | Partially Covered |
| SCM-006 | AC2 | TP_SCM6_005 Status Fail; Actual Result: Adjusted billing amount absent in downgrade notification; Defect ID & Description: DEF-SCM6-101 - Adjusted billing amount not included in downgrade confirmation notification to customer | Partially Covered |
| SCM-006 | AC4 | TP_SCM6_012 Status Fail; Actual Result: Audit log entry missing when credit issued is $0; Defect ID & Description: DEF-SCM6-102 - Audit log not created when downgrade results in zero credit amount; No mapped testcase explicitly validates previous plan capture in the audit log; No mapped testcase explicitly validates downgraded plan capture in the audit log; No mapped testcase explicitly validates effective date capture in the audit log; No mapped testcase explicitly validates timestamp capture in the audit log | Partially Covered |
| SCM-006 | AC5 | TP_SCM6_015 Status Fail; Actual Result: Downgrade processed without waiting for account manager approval; Defect ID & Description: DEF-SCM6-103 - Enterprise downgrade not held pending state; processed immediately bypassing approval workflow; No mapped testcase explicitly validates customer retention review requirement | Partially Covered |
| SCM-007 | AC2 | TP_SCM7_005 Status Fail; Actual Result: New owner notification not sent in all transfer scenarios; Defect ID & Description: DEF-SCM7-101 - New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint; No mapped testcase explicitly validates transfer details inclusion in the notification | Partially Covered |
| SCM-007 | AC3 | No mapped testcase explicitly validates billing change summary visibility in the customer portal | Partially Covered |
| SCM-007 | AC4 | TP_SCM7_014 Status Fail; Actual Result: Authorization reference blank for bulk API-initiated transfers in audit log; Defect ID & Description: DEF-SCM7-103 - Audit log authorization reference field empty when transfer initiated via bulk admin API; No mapped testcase explicitly validates subscription ID capture in the transfer audit log; No mapped testcase explicitly validates transfer date capture in the transfer audit log; No mapped testcase explicitly validates timestamp capture in the transfer audit log | Partially Covered |
| SCM-007 | AC5 | No mapped testcase explicitly validates billing entity change compliance approval requirement; TP_SCM7_012 Status Fail; Actual Result: Transfer not flagged when only tax jurisdiction changes without entity change; Defect ID & Description: DEF-SCM7-102 - Compliance approval workflow not initiated for transfers involving tax jurisdiction change only without entity change | Partially Covered |

## Consistency Analysis

`mapping_consistency_details` contains only direct mappings (no missing_testcase or missing_testlog entries). As there are no mapping inconsistencies recorded, and per the rule that this subsection should appear only when such rows exist, **no “Data Mapping Inconsistency Details” table is generated.**

### Consistency Metrics Summary

| Metric | Count |
|---|---|
| total_testcases | 102 |
| total_testlogs | 100 |
| consistency_status | Inconsistent |
| missing_testlogs | 2 |
| missing_testcases | 0 |

## Defect Details

Defect Details are sourced exclusively from:
`coverage_analysis[*].acceptance_criteria_details[*].defect_details[*]`.

### Defect Details

| Defect ID | Test Case ID | User Story ID | Defect Description |
|---|---|---|---|
| DEF-SCM1-001 | UT_SCM1_005 | SCM-001 | Notification template rendering issue |
| DEF-SCM1-002 | UT_SCM1_009 | SCM-001 | Refund workflow synchronization error |
| DEF-SCM2-101 | TP_SCM2_008 | SCM-002 | Pause reason not captured consistently |
| DEF-SCM2-102 | TP_SCM2_009 | SCM-002 | Activation allowed without completed approval |
| DEF-SCM3-101 | TP_SCM3_004 | SCM-003 | Revised billing amount not included in upgrade confirmation notification |
| DEF-SCM3-102 | TP_SCM3_009 | SCM-003 | Manager approval workflow not initiated when price increase equals exactly 50% |
| DEF-SCM4-101 | TP_SCM4_004 | SCM-004 | Applicable refund details not included in cancellation confirmation notification |
| DEF-SCM4-102 | TP_SCM4_009 | SCM-004 | Finance team approval workflow fails for mixed currency outstanding balances |
| DEF-SCM5-103 | TP_SCM5_011 | SCM-005 | System sends reminder even when subscription expiry date is null |
| DEF-SCM5-101 | TP_SCM5_005 | SCM-005 | Renewal amount not populated in 30-day reminder notification for monthly billing plans |
| DEF-SCM5-105 | TP_SCM5_015 | SCM-005 | Reminder log delivery status remains blank when notification channel fails |
| DEF-SCM5-104 | TP_SCM5_013 | SCM-005 | Boundary condition error: $10,000 subscription flagged as high-value instead of requiring value >$10,000 |
| DEF-SCM6-101 | TP_SCM6_005 | SCM-006 | Adjusted billing amount not included in downgrade confirmation notification to customer |
| DEF-SCM6-102 | TP_SCM6_012 | SCM-006 | Audit log not created when downgrade results in zero credit amount |
| DEF-SCM6-103 | TP_SCM6_015 | SCM-006 | Enterprise downgrade not held pending state; processed immediately bypassing approval workflow |
| DEF-SCM7-101 | TP_SCM7_005 | SCM-007 | New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint |
| DEF-SCM7-101 | TP_SCM7_015 | SCM-007 | New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint |
| DEF-SCM7-103 | TP_SCM7_014 | SCM-007 | Audit log authorization reference field empty when transfer initiated via bulk admin API |
| DEF-SCM7-102 | TP_SCM7_012 | SCM-007 | Compliance approval workflow not initiated for transfers involving tax jurisdiction change only without entity change |

## Conclusion

At least one acceptance criterion per user story is marked as “Partially Covered”, and multiple defects are recorded; therefore, remediation is required before progression based on the provided unit test coverage and quality data.
