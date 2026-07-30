# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 9 user stories (SCM-001 to SCM-009) based on the structured coverage_analysis JSON provided by the upstream Deterministic Requirement And Coverage Intelligence Agent. These user stories form the baseline for all metrics and observations in this report.

The scope is restricted to:

- Unit test cases and related test artifacts that are explicitly mapped to the above user stories and their acceptance criteria.
- Coverage status per acceptance criterion (Fully Covered, Partially Covered, Not Covered) as supplied in coverage_analysis.
- Explicit coverage gaps as supplied in coverage_gaps under each acceptance criterion.
- Defect records explicitly supplied in defect_details under each acceptance criterion.
- Mapping consistency and execution consistency as supplied in mapping_consistency_details and consistency_summary.

Inclusions:

- Unit test cases linked to the identified user stories and acceptance criteria.
- Test coverage status and documented coverage gaps per acceptance criterion.
- Defect data directly associated with these user stories via coverage_analysis[*].acceptance_criteria_details[*].defect_details[*].
- Consistency metrics and mapping details from mapping_consistency_details and consistency_summary.

Exclusions:

- Integration tests, system tests, performance tests, or any non-unit testing activities.
- Any user stories or acceptance criteria not present in the provided coverage_analysis JSON.
- Any defects or execution outcomes not present in defect_details under coverage_analysis.
- Any additional recalculated coverage, inferred gaps, or synthetic metrics beyond what is explicitly present in the JSON.

The user stories and their acceptance criteria, as represented in coverage_analysis, constitute the baseline reference for measuring unit test coverage, execution consistency, and defect-related quality.

## Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-001 | AC2 | UT_SCM1_005 execution result is Fail; Actual Result: Notification content generation failed; Defect: DEF-SCM1-001 - Notification template rendering issue | Partially Covered |
| SCM-001 | AC5 | UT_SCM1_009 execution result is Fail; Actual Result: High-value refund processing blocked; Defect: DEF-SCM1-002 - Refund workflow synchronization error | Partially Covered |
| SCM-001 | AC5 | No mapped testcase explicitly validates fraud review; UT_SCM1_009 references manager approval workflow only; UT_SCM1_013 and UT_SCM1_015 reference approval workflow only | Partially Covered |
| SCM-002 | AC2 | No mapped testcase explicitly validates resume date inclusion; TP_SCM2_004 validates notification sent; TP_SCM2_005 validates pause start date only; TP_SCM2_011 validates notification suppression when email is missing | Partially Covered |
| SCM-002 | AC3 | No mapped testcase explicitly validates scheduled resume date in portal; TP_SCM2_006 validates pause status only; TP_SCM2_007 validates pause history only | Partially Covered |
| SCM-002 | AC4 | TP_SCM2_008 execution result is Fail; Actual Result: Pause reason missing in some records; Defect: DEF-SCM2-101 - Pause reason not captured consistently | Partially Covered |
| SCM-002 | AC4 | TP_SCM2_008 execution result is Fail; Actual Result: Pause reason missing in some records; Defect: DEF-SCM2-101 - Pause reason not captured consistently | Partially Covered |
| SCM-002 | AC4 | TP_SCM2_008 execution result is Fail; Actual Result: Pause reason missing in some records; Defect: DEF-SCM2-101 - Pause reason not captured consistently | Partially Covered |
| SCM-002 | AC4 | TP_SCM2_008 execution result is Fail; Actual Result: Pause reason missing in some records; Defect: DEF-SCM2-101 - Pause reason not captured consistently | Partially Covered |
| SCM-002 | AC4 | TP_SCM2_008 execution result is Fail; Actual Result: Pause reason missing in some records; Defect: DEF-SCM2-101 - Pause reason not captured consistently | Partially Covered |
| SCM-002 | AC5 | TP_SCM2_009 execution result is Fail; Actual Result: Pause activated before approval validation; Defect: DEF-SCM2-102 - Activation allowed without completed approval | Partially Covered |
| SCM-002 | AC5 | TP_SCM2_009 execution result is Fail; Actual Result: Pause activated before approval validation; Defect: DEF-SCM2-102 - Activation allowed without completed approval | Partially Covered |
| SCM-003 | AC2 | TP_SCM3_004 execution result is Fail; Actual Result: Revised billing amount missing in notification; Defect: DEF-SCM3-101 - Revised billing amount not included in upgrade confirmation notification | Partially Covered |
| SCM-003 | AC2 | TP_SCM3_004 execution result is Fail; Actual Result: Revised billing amount missing in notification; Defect: DEF-SCM3-101 - Revised billing amount not included in upgrade confirmation notification | Partially Covered |
| SCM-003 | AC2 | TP_SCM3_004 execution result is Fail; Actual Result: Revised billing amount missing in notification; Defect: DEF-SCM3-101 - Revised billing amount not included in upgrade confirmation notification | Partially Covered |
| SCM-003 | AC2 | TP_SCM3_004 execution result is Fail; Actual Result: Revised billing amount missing in notification; Defect: DEF-SCM3-101 - Revised billing amount not included in upgrade confirmation notification | Partially Covered |
| SCM-003 | AC3 | No mapped testcase explicitly validates next billing cycle changes in the portal; TP_SCM3_006 validates upgrade request status only; TP_SCM3_007 validates upgrade history only | Partially Covered |
| SCM-003 | AC5 | TP_SCM3_009 execution result is Fail; Actual Result: Approval workflow not triggered for borderline 50% cases; Defect: DEF-SCM3-102 - Manager approval workflow not initiated when price increase equals exactly 50% | Partially Covered |
| SCM-003 | AC5 | No mapped testcase explicitly validates that approval must occur before activation; TP_SCM3_009 validates approval workflow initiation and failed; TP_SCM3_013 validates no approval below 50% | Partially Covered |
| SCM-004 | AC2 | TP_SCM4_004 execution result is Fail; Actual Result: Refund details missing from cancellation notification; Defect: DEF-SCM4-101 - Applicable refund details not included in cancellation confirmation notification | Partially Covered |
| SCM-004 | AC2 | TP_SCM4_004 execution result is Fail; Actual Result: Refund details missing from cancellation notification; Defect: DEF-SCM4-101 - Applicable refund details not included in cancellation confirmation notification | Partially Covered |
| SCM-004 | AC2 | TP_SCM4_004 execution result is Fail; Actual Result: Refund details missing from cancellation notification; Defect: DEF-SCM4-101 - Applicable refund details not included in cancellation confirmation notification | Partially Covered |
| SCM-004 | AC5 | TP_SCM4_009 execution result is Fail; Actual Result: Finance approval workflow not triggered consistently; Defect: DEF-SCM4-102 - Finance team approval workflow fails for mixed currency outstanding balances | Partially Covered |
| SCM-004 | AC5 | No mapped testcase explicitly validates that finance approval must occur before processing; TP_SCM4_009 validates workflow initiation and failed; TP_SCM4_013 and TP_SCM4_015 validate approval trigger conditions | Partially Covered |
| SCM-005 | AC1 | TP_SCM5_011 execution result is Fail; Actual Result: Reminder still triggered despite missing expiry date, no error logged; Defect: DEF-SCM5-103 - System sends reminder even when subscription expiry date is null | Partially Covered |
| SCM-005 | AC1 | TP_SCM5_011 execution result is Fail; Actual Result: Reminder still triggered despite missing expiry date, no error logged; Defect: DEF-SCM5-103 - System sends reminder even when subscription expiry date is null | Partially Covered |
| SCM-005 | AC1 | TP_SCM5_011 execution result is Fail; Actual Result: Reminder still triggered despite missing expiry date, no error logged; Defect: DEF-SCM5-103 - System sends reminder even when subscription expiry date is null | Partially Covered |
| SCM-005 | AC2 | TP_SCM5_005 execution result is Fail; Actual Result: Renewal amount missing in 30-day reminder notification; Defect: DEF-SCM5-101 - Renewal amount not populated in 30-day reminder notification for monthly billing plans | Partially Covered |
| SCM-005 | AC2 | TP_SCM5_005 execution result is Fail; Actual Result: Renewal amount missing in 30-day reminder notification; Defect: DEF-SCM5-101 - Renewal amount not populated in 30-day reminder notification for monthly billing plans | Partially Covered |
| SCM-005 | AC2 | TP_SCM5_005 execution result is Fail; Actual Result: Renewal amount missing in 30-day reminder notification; Defect: DEF-SCM5-101 - Renewal amount not populated in 30-day reminder notification for monthly billing plans | Partially Covered |
| SCM-005 | AC2 | TP_SCM5_005 execution result is Fail; Actual Result: Renewal amount missing in 30-day reminder notification; Defect: DEF-SCM5-101 - Renewal amount not populated in 30-day reminder notification for monthly billing plans | Partially Covered |
| SCM-005 | AC4 | TP_SCM5_015 execution result is Fail; Actual Result: Delivery status not updated to Failed when email channel is unavailable; Defect: DEF-SCM5-105 - Reminder log delivery status remains blank when notification channel fails | Partially Covered |
| SCM-005 | AC4 | TP_SCM5_015 execution result is Fail; Actual Result: Delivery status not updated to Failed when email channel is unavailable; Defect: DEF-SCM5-105 - Reminder log delivery status remains blank when notification channel fails | Partially Covered |
| SCM-005 | AC4 | No mapped testcase explicitly validates reminder date capture; TP_SCM5_010 validates customer ID and subscription ID only; TP_SCM5_015 failed on delivery status | Partially Covered |
| SCM-005 | AC4 | No mapped testcase explicitly validates channel used capture; TP_SCM5_010 validates customer ID and subscription ID only; TP_SCM5_015 failed on delivery status | Partially Covered |
| SCM-005 | AC4 | TP_SCM5_015 execution result is Fail; Actual Result: Delivery status not updated to Failed when email channel is unavailable; Defect: DEF-SCM5-105 - Reminder log delivery status remains blank when notification channel fails | Partially Covered |
| SCM-005 | AC5 | TP_SCM5_013 execution result is Fail; Actual Result: Subscription at exactly $10,000 incorrectly flagged as high-value; Defect: DEF-SCM5-104 - Boundary condition error: $10,000 subscription flagged as high-value instead of requiring value >$10,000 | Partially Covered |
| SCM-005 | AC5 | TP_SCM5_013 execution result is Fail; Actual Result: Subscription at exactly $10,000 incorrectly flagged as high-value; Defect: DEF-SCM5-104 - Boundary condition error: $10,000 subscription flagged as high-value instead of requiring value >$10,000 | Partially Covered |
| SCM-006 | AC2 | TP_SCM6_005 execution result is Fail; Actual Result: Adjusted billing amount absent in downgrade notification; Defect: DEF-SCM6-101 - Adjusted billing amount not included in downgrade confirmation notification to customer | Partially Covered |
| SCM-006 | AC2 | TP_SCM6_005 execution result is Fail; Actual Result: Adjusted billing amount absent in downgrade notification; Defect: DEF-SCM6-101 - Adjusted billing amount not included in downgrade confirmation notification to customer | Partially Covered |
| SCM-006 | AC2 | TP_SCM6_005 execution result is Fail; Actual Result: Adjusted billing amount absent in downgrade notification; Defect: DEF-SCM6-101 - Adjusted billing amount not included in downgrade confirmation notification to customer | Partially Covered |
| SCM-006 | AC2 | TP_SCM6_005 execution result is Fail; Actual Result: Adjusted billing amount absent in downgrade notification; Defect: DEF-SCM6-101 - Adjusted billing amount not included in downgrade confirmation notification to customer | Partially Covered |
| SCM-006 | AC4 | TP_SCM6_012 execution result is Fail; Actual Result: Audit log entry missing when credit issued is $0; Defect: DEF-SCM6-102 - Audit log not created when downgrade results in zero credit amount | Partially Covered |
| SCM-006 | AC4 | TP_SCM6_012 execution result is Fail; Actual Result: Audit log entry missing when credit issued is $0; Defect: DEF-SCM6-102 - Audit log not created when downgrade results in zero credit amount | Partially Covered |
| SCM-006 | AC4 | TP_SCM6_012 execution result is Fail; Actual Result: Audit log entry missing when credit issued is $0; Defect: DEF-SCM6-102 - Audit log not created when downgrade results in zero credit amount | Partially Covered |
| SCM-006 | AC4 | TP_SCM6_012 execution result is Fail; Actual Result: Audit log entry missing when credit issued is $0; Defect: DEF-SCM6-102 - Audit log not created when downgrade results in zero credit amount | Partially Covered |
| SCM-006 | AC4 | TP_SCM6_012 execution result is Fail; Actual Result: Audit log entry missing when credit issued is $0; Defect: DEF-SCM6-102 - Audit log not created when downgrade results in zero credit amount | Partially Covered |
| SCM-006 | AC4 | TP_SCM6_012 execution result is Fail; Actual Result: Audit log entry missing when credit issued is $0; Defect: DEF-SCM6-102 - Audit log not created when downgrade results in zero credit amount | Partially Covered |
| SCM-006 | AC4 | TP_SCM6_012 execution result is Fail; Actual Result: Audit log entry missing when credit issued is $0; Defect: DEF-SCM6-102 - Audit log not created when downgrade results in zero credit amount | Partially Covered |
| SCM-006 | AC5 | TP_SCM6_015 execution result is Fail; Actual Result: Downgrade processed without waiting for account manager approval; Defect: DEF-SCM6-103 - Enterprise downgrade not held pending state; processed immediately bypassing approval workflow | Partially Covered |
| SCM-006 | AC5 | No mapped testcase explicitly validates customer retention review execution; TP_SCM6_013 validates enterprise downgrade flagged correctly; TP_SCM6_014 validates account manager approval workflow only; TP_SCM6_015 failed on pending approval processing | Partially Covered |
| SCM-006 | AC5 | TP_SCM6_015 execution result is Fail; Actual Result: Downgrade processed without waiting for account manager approval; Defect: DEF-SCM6-103 - Enterprise downgrade not held pending state; processed immediately bypassing approval workflow | Partially Covered |
| SCM-007 | AC2 | TP_SCM7_005 execution result is Fail; Actual Result: New owner notification not sent in all transfer scenarios; Defect: DEF-SCM7-101 - New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint | Partially Covered |
| SCM-007 | AC2 | TP_SCM7_005 execution result is Fail; Actual Result: New owner notification not sent in all transfer scenarios; Defect: DEF-SCM7-101 - New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint | Partially Covered |
| SCM-007 | AC2 | No mapped testcase explicitly validates transfer details content; TP_SCM7_006 validates effective date and billing responsibility only; TP_SCM7_005 and TP_SCM7_015 failed on new owner notification | Partially Covered |
| SCM-007 | AC2 | TP_SCM7_005 execution result is Fail; Actual Result: New owner notification not sent in all transfer scenarios; Defect: DEF-SCM7-101 - New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint | Partially Covered |
| SCM-007 | AC2 | TP_SCM7_005 execution result is Fail; Actual Result: New owner notification not sent in all transfer scenarios; Defect: DEF-SCM7-101 - New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint | Partially Covered |
| SCM-007 | AC3 | No mapped testcase explicitly validates billing change summary in the customer portal; TP_SCM7_007 validates outgoing owner transfer status; TP_SCM7_008 validates incoming owner transfer status; TP_SCM7_009 validates ownership history | Partially Covered |
| SCM-007 | AC4 | TP_SCM7_014 execution result is Fail; Actual Result: Authorization reference blank for bulk API-initiated transfers in audit log; Defect: DEF-SCM7-103 - Audit log authorization reference field empty when transfer initiated via bulk admin API | Partially Covered |
| SCM-007 | AC4 | TP_SCM7_014 execution result is Fail; Actual Result: Authorization reference blank for bulk API-initiated transfers in audit log; Defect: DEF-SCM7-103 - Audit log authorization reference field empty when transfer initiated via bulk admin API | Partially Covered |
| SCM-007 | AC4 | No mapped testcase explicitly validates subscription ID in transfer audit log; TP_SCM7_010 validates current and new owner IDs only; TP_SCM7_014 failed on authorization reference | Partially Covered |
| SCM-007 | AC4 | No mapped testcase explicitly validates transfer date in transfer audit log; TP_SCM7_010 validates current and new owner IDs only; TP_SCM7_014 failed on authorization reference | Partially Covered |
| SCM-007 | AC4 | TP_SCM7_014 execution result is Fail; Actual Result: Authorization reference blank for bulk API-initiated transfers in audit log; Defect: DEF-SCM7-103 - Audit log authorization reference field empty when transfer initiated via bulk admin API | Partially Covered |
| SCM-007 | AC4 | No mapped testcase explicitly validates timestamp in transfer audit log; TP_SCM7_010 validates current and new owner IDs only; TP_SCM7_014 failed on authorization reference | Partially Covered |
| SCM-007 | AC5 | No mapped testcase explicitly validates billing entity change path; TP_SCM7_012 failed for tax jurisdiction change only; TP_SCM7_013 validates pending approval blocking only | Partially Covered |
| SCM-007 | AC5 | TP_SCM7_012 execution result is Fail; Actual Result: Transfer not flagged when only tax jurisdiction changes without entity change; Defect: DEF-SCM7-102 - Compliance approval workflow not initiated for transfers involving tax jurisdiction change only without entity change | Partially Covered |
| SCM-007 | AC5 | TP_SCM7_012 execution result is Fail; Actual Result: Transfer not flagged when only tax jurisdiction changes without entity change; Defect: DEF-SCM7-102 - Compliance approval workflow not initiated for transfers involving tax jurisdiction change only without entity change | Partially Covered |
| SCM-008 | AC1 | UT_SCM8_003 execution result is Failed; Actual Result: Points posting delayed; Defect: DEF-SCM8-001 - Points posting service delay | Partially Covered |
| SCM-008 | AC2 | UT_SCM8_014 execution result is Pending; Actual Result: Zero-point redemption rejection not yet executed | Partially Covered |
| SCM-008 | AC3 | UT_SCM8_007 execution result is Failed; Actual Result: Balance refresh issue observed; Defect: DEF-SCM8-002 - Balance refresh cache issue | Partially Covered |
| SCM-008 | AC5 | UT_SCM8_009 execution result is Failed; Actual Result: High value workflow validation failed; Defect: DEF-SCM8-003 - Redemption workflow synchronization issue | Partially Covered |
| SCM-008 | AC5 | No mapped testcase explicitly validates fraud review; TP_SCM8_009, TP_SCM8_013, and TP_SCM8_015 reference manager approval workflow only | Partially Covered |
| SCM-009 | AC2 | UT_SCM9_004 execution result is Fail; Actual Result: SMS not delivered; Defect: DEF-SCM9-001 - SMS gateway timeout prevents delivery | Partially Covered |
| SCM-009 | AC2 | UT_SCM9_014 execution result is Pending; Actual Result: International SMS delivery test not yet executed | Partially Covered |
| SCM-009 | AC3 | UT_SCM9_012 execution result is Fail; Actual Result: Push notification dispatched despite user disabling channel; Defect: DEF-SCM9-002 - Push notification service ignores user preference flag | Partially Covered |
| SCM-009 | AC5 | UT_SCM9_015 execution result is Pending; Actual Result: 3rd-of-3 retry boundary test not yet executed | Partially Covered |

## Consistency Analysis

Consistency analysis is based exclusively on:

- mapping_consistency_details
- consistency_summary

No recalculation or inference of additional inconsistencies is performed.

## Data Mapping Inconsistency Details

No data available in the input.

## Consistency Metrics Summary

| Metric | Count |
|---|---|
| total_testcases | 132 |
| total_testlogs | 132 |
| missing_testlogs | 0 |
| missing_testcases | 0 |
| consistency_status | Consistent |

## Defect Details

Defect details are sourced exclusively from:

- coverage_analysis[*].acceptance_criteria_details[*].defect_details[*]

No defects are derived from execution data, coverage gaps, or other sections.

## Defect Details

| Defect ID | Test Case ID | User Story ID | Defect Description |
|---|---|---|---|
| DEF-SCM1-001 | UT_SCM1_005 | SCM-001 | DEF-SCM1-001 - Notification template rendering issue |
| DEF-SCM1-002 | UT_SCM1_009 | SCM-001 | DEF-SCM1-002 - Refund workflow synchronization error |
| DEF-SCM2-101 | TP_SCM2_008 | SCM-002 | DEF-SCM2-101 - Pause reason not captured consistently |
| DEF-SCM2-102 | TP_SCM2_009 | SCM-002 | DEF-SCM2-102 - Activation allowed without completed approval |
| DEF-SCM3-101 | TP_SCM3_004 | SCM-003 | DEF-SCM3-101 - Revised billing amount not included in upgrade confirmation notification |
| DEF-SCM3-102 | TP_SCM3_009 | SCM-003 | DEF-SCM3-102 - Manager approval workflow not initiated when price increase equals exactly 50% |
| DEF-SCM4-101 | TP_SCM4_004 | SCM-004 | DEF-SCM4-101 - Applicable refund details not included in cancellation confirmation notification |
| DEF-SCM4-102 | TP_SCM4_009 | SCM-004 | DEF-SCM4-102 - Finance team approval workflow fails for mixed currency outstanding balances |
| DEF-SCM5-103 | TP_SCM5_011 | SCM-005 | DEF-SCM5-103 - System sends reminder even when subscription expiry date is null |
| DEF-SCM5-101 | TP_SCM5_005 | SCM-005 | DEF-SCM5-101 - Renewal amount not populated in 30-day reminder notification for monthly billing plans |
| DEF-SCM5-105 | TP_SCM5_015 | SCM-005 | DEF-SCM5-105 - Reminder log delivery status remains blank when notification channel fails |
| DEF-SCM5-104 | TP_SCM5_013 | SCM-005 | DEF-SCM5-104 - Boundary condition error: $10,000 subscription flagged as high-value instead of requiring value >$10,000 |
| DEF-SCM6-101 | TP_SCM6_005 | SCM-006 | DEF-SCM6-101 - Adjusted billing amount not included in downgrade confirmation notification to customer |
| DEF-SCM6-102 | TP_SCM6_012 | SCM-006 | DEF-SCM6-102 - Audit log not created when downgrade results in zero credit amount |
| DEF-SCM6-103 | TP_SCM6_015 | SCM-006 | DEF-SCM6-103 - Enterprise downgrade not held pending state; processed immediately bypassing approval workflow |
| DEF-SCM7-101 | TP_SCM7_005 | SCM-007 | DEF-SCM7-101 - New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint |
| DEF-SCM7-101 | TP_SCM7_015 | SCM-007 | DEF-SCM7-101 - New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint |
| DEF-SCM7-103 | TP_SCM7_014 | SCM-007 | DEF-SCM7-103 - Audit log authorization reference field empty when transfer initiated via bulk admin API |
| DEF-SCM7-102 | TP_SCM7_012 | SCM-007 | DEF-SCM7-102 - Compliance approval workflow not initiated for transfers involving tax jurisdiction change only without entity change |
| DEF-SCM8-001 | UT_SCM8_003 | SCM-008 | DEF-SCM8-001 - Points posting service delay |
| DEF-SCM8-002 | UT_SCM8_007 | SCM-008 | DEF-SCM8-002 - Balance refresh cache issue |
| DEF-SCM8-003 | UT_SCM8_009 | SCM-008 | DEF-SCM8-003 - Redemption workflow synchronization issue |
| DEF-SCM9-001 | UT_SCM9_004 | SCM-009 | DEF-SCM9-001 - SMS gateway timeout prevents delivery |
| DEF-SCM9-002 | UT_SCM9_012 | SCM-009 | DEF-SCM9-002 - Push notification service ignores user preference flag |

## Conclusion

At least one acceptance criterion per user story is Partially Covered, and multiple defects are recorded across SCM-001 to SCM-009; therefore, remediation is required before progression, based on the provided unit test coverage and defect data.
