# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 9 user stories (SCM-001 to SCM-009) based on the structured JSON provided by the Deterministic Requirement And Coverage Intelligence Agent.

These 9 user stories form the baseline for evaluation. The scope is restricted to unit test plans, coverage data, and execution records mapped to these user stories. All metrics, gaps, and defects are sourced directly from the provided JSON; no values are recalculated or inferred.

## Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-001 | AC2 | UT_SCM1_005 status is Fail. Actual Result: Notification content generation failed. Defect: DEF-SCM1-001 - Notification template rendering issue | Partially Covered |
| SCM-001 | AC5 | UT_SCM1_009 status is Fail. Actual Result: High-value refund processing blocked. Defect: DEF-SCM1-002 - Refund workflow synchronization error |
No mapped testcase explicitly validates fraud review in the artifacts. | Partially Covered |
| SCM-002 | AC2 | No mapped testcase explicitly validates resume date inclusion in the artifacts. | Partially Covered |
| SCM-002 | AC3 | No mapped testcase explicitly validates scheduled resume date visibility in the artifacts. | Partially Covered |
| SCM-002 | AC4 | TP_SCM2_008 status is Fail. Actual Result: Pause reason missing in some records. Defect: DEF-SCM2-101 - Pause reason not captured consistently |
No mapped testcase explicitly validates pause start date capture in the artifacts. | Partially Covered |
| SCM-002 | AC5 | TP_SCM2_009 status is Fail. Actual Result: Pause activated before approval validation. Defect: DEF-SCM2-102 - Activation allowed without completed approval | Partially Covered |
| SCM-003 | AC2 | TP_SCM3_004 status is Fail. Actual Result: Revised billing amount missing in notification. Defect: DEF-SCM3-101 - Revised billing amount not included in upgrade confirmation notification | Partially Covered |
| SCM-003 | AC3 | No mapped testcase explicitly validates next billing cycle changes visibility in the artifacts. | Partially Covered |
| SCM-003 | AC5 | TP_SCM3_009 status is Fail. Actual Result: Approval workflow not triggered for borderline 50% cases. Defect: DEF-SCM3-102 - Manager approval workflow not initiated when price increase equals exactly 50% |
No mapped testcase explicitly validates activation is blocked until approval in the artifacts. | Partially Covered |
| SCM-004 | AC2 | TP_SCM4_004 status is Fail. Actual Result: Refund details missing from cancellation notification. Defect: DEF-SCM4-101 - Applicable refund details not included in cancellation confirmation notification | Partially Covered |
| SCM-004 | AC5 | TP_SCM4_009 status is Fail. Actual Result: Finance approval workflow not triggered consistently. Defect: DEF-SCM4-102 - Finance team approval workflow fails for mixed currency outstanding balances |
No mapped testcase explicitly validates cancellation is blocked until finance approval in the artifacts. | Partially Covered |
| SCM-005 | AC1 | TP_SCM5_011 status is Fail. Actual Result: Reminder still triggered despite missing expiry date, no error logged. Defect: DEF-SCM5-103 - System sends reminder even when subscription expiry date is null | Partially Covered |
| SCM-005 | AC2 | TP_SCM5_005 status is Fail. Actual Result: Renewal amount missing in 30-day reminder notification. Defect: DEF-SCM5-101 - Renewal amount not populated in 30-day reminder notification for monthly billing plans | Partially Covered |
| SCM-005 | AC4 | TP_SCM5_015 status is Fail. Actual Result: Delivery status not updated to Failed when email channel is unavailable. Defect: DEF-SCM5-105 - Reminder log delivery status remains blank when notification channel fails |
No mapped testcase explicitly validates reminder date capture in the artifacts. |
No mapped testcase explicitly validates channel used capture in the artifacts. | Partially Covered |
| SCM-005 | AC5 | No mapped testcase explicitly validates customer reminder for high-value subscriptions in the artifacts. |
TP_SCM5_013 status is Fail. Actual Result: Subscription at exactly $10,000 incorrectly flagged as high-value. Defect: DEF-SCM5-104 - Boundary condition error: $10,000 subscription flagged as high-value instead of requiring value >$10,000 | Partially Covered |
| SCM-006 | AC2 | TP_SCM6_005 status is Fail. Actual Result: Adjusted billing amount absent in downgrade notification. Defect: DEF-SCM6-101 - Adjusted billing amount not included in downgrade confirmation notification to customer | Partially Covered |
| SCM-006 | AC4 | TP_SCM6_012 status is Fail. Actual Result: Audit log entry missing when credit issued is $0. Defect: DEF-SCM6-102 - Audit log not created when downgrade results in zero credit amount | Partially Covered |
| SCM-006 | AC5 | TP_SCM6_015 status is Fail. Actual Result: Downgrade processed without waiting for account manager approval. Defect: DEF-SCM6-103 - Enterprise downgrade not held pending state; processed immediately bypassing approval workflow |
No mapped testcase explicitly validates customer retention review in the artifacts. | Partially Covered |
| SCM-007 | AC2 | TP_SCM7_005 status is Fail. Actual Result: New owner notification not sent in all transfer scenarios. Defect: DEF-SCM7-101 - New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint |
TP_SCM7_015 status is Fail. Actual Result: New owner notification not sent for bulk API transfer. Defect: DEF-SCM7-101 - New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint |
No mapped testcase explicitly validates transfer details inclusion in the artifacts. | Partially Covered |
| SCM-007 | AC3 | No mapped testcase explicitly validates billing change summary visibility in the artifacts. | Partially Covered |
| SCM-007 | AC4 | TP_SCM7_014 status is Fail. Actual Result: Authorization reference blank for bulk API-initiated transfers in audit log. Defect: DEF-SCM7-103 - Audit log authorization reference field empty when transfer initiated via bulk admin API |
No mapped testcase explicitly validates subscription ID capture in the artifacts. |
No mapped testcase explicitly validates transfer date capture in the artifacts. |
No mapped testcase explicitly validates timestamp capture in the artifacts. | Partially Covered |
| SCM-007 | AC5 | No mapped testcase explicitly validates billing entity change approval in the artifacts. |
TP_SCM7_012 status is Fail. Actual Result: Transfer not flagged when only tax jurisdiction changes without entity change. Defect: DEF-SCM7-102 - Compliance approval workflow not initiated for transfers involving tax jurisdiction change only without entity change | Partially Covered |
| SCM-008 | AC1 | No execution log testcase ID exactly matches mapped testcase IDs. Mapped testcases use TP_SCM8_* while execution logs use UT_SCM8_*. | Not Covered |
| SCM-008 | AC2 | No execution log testcase ID exactly matches mapped testcase IDs. Mapped testcases use TP_SCM8_* while execution logs use UT_SCM8_*. | Not Covered |
| SCM-008 | AC3 | No execution log testcase ID exactly matches mapped testcase IDs. Mapped testcases use TP_SCM8_* while execution logs use UT_SCM8_*. | Not Covered |
| SCM-008 | AC4 | No execution log testcase ID exactly matches mapped testcase IDs. Mapped testcases use TP_SCM8_* while execution logs use UT_SCM8_*. | Not Covered |
| SCM-008 | AC5 | No execution log testcase ID exactly matches mapped testcase IDs. Mapped testcases use TP_SCM8_* while execution logs use UT_SCM8_*. | Not Covered |
| SCM-009 | AC2 | UT_SCM9_004 status is Fail. Actual Result: SMS not delivered. Defect: DEF-SCM9-001 - SMS gateway timeout prevents delivery | Partially Covered |
| SCM-009 | AC3 | UT_SCM9_012 status is Fail. Actual Result: Push notification dispatched despite user disabling channel. Defect: DEF-SCM9-002 - Push notification service ignores user preference flag | Partially Covered |

## Consistency Analysis

Per instructions, this section is populated directly from the input.

## Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| UT_SCM1_001 | Direct | Testcase directly maps to AC1 | SCM-001 | AC1 | Low |
| UT_SCM1_002 | Direct | Testcase directly maps to AC1 | SCM-001 | AC1 | Low |
| UT_SCM1_003 | Direct | Testcase directly maps to AC1 | SCM-001 | AC1 | Low |
| UT_SCM1_004 | Direct | Testcase directly maps to AC2 | SCM-001 | AC2 | Low |
| UT_SCM1_005 | Direct | Testcase directly maps to AC2 | SCM-001 | AC2 | High |
| UT_SCM1_006 | Direct | Testcase directly maps to AC3 | SCM-001 | AC3 | Low |
| UT_SCM1_007 | Direct | Testcase directly maps to AC3 | SCM-001 | AC3 | Low |
| UT_SCM1_008 | Direct | Testcase directly maps to AC4 | SCM-001 | AC4 | Low |
| UT_SCM1_009 | Direct | Testcase directly maps to AC5 | SCM-001 | AC5 | High |
| UT_SCM1_010 | Direct | Testcase directly maps to AC1 | SCM-001 | AC1 | Low |
| UT_SCM1_011 | Direct | Testcase directly maps to AC2 | SCM-001 | AC2 | Low |
| UT_SCM1_012 | Direct | Testcase directly maps to AC4 | SCM-001 | AC4 | Low |
| UT_SCM1_013 | Direct | Testcase directly maps to AC5 | SCM-001 | AC5 | Low |
| UT_SCM1_014 | Direct | Testcase directly maps to AC2 | SCM-001 | AC2 | Low |
| UT_SCM1_015 | Direct | Testcase directly maps to AC5 | SCM-001 | AC5 | Low |
| TP_SCM2_001 | Direct | Testcase directly maps to AC1 | SCM-002 | AC1 | Low |
| TP_SCM2_002 | Direct | Testcase directly maps to AC1 | SCM-002 | AC1 | Low |
| TP_SCM2_003 | Direct | Testcase directly maps to AC1 | SCM-002 | AC1 | Low |
| TP_SCM2_004 | Direct | Testcase directly maps to AC2 | SCM-002 | AC2 | Low |
| TP_SCM2_005 | Direct | Testcase directly maps to AC2 | SCM-002 | AC2 | Low |
| TP_SCM2_006 | Direct | Testcase directly maps to AC3 | SCM-002 | AC3 | Low |
| TP_SCM2_007 | Direct | Testcase directly maps to AC3 | SCM-002 | AC3 | Low |
| TP_SCM2_008 | Direct | Testcase directly maps to AC4 | SCM-002 | AC4 | High |
| TP_SCM2_009 | Direct | Testcase directly maps to AC5 | SCM-002 | AC5 | High |
| TP_SCM2_010 | Direct | Testcase directly maps to AC1 | SCM-002 | AC1 | Low |
| TP_SCM2_011 | Direct | Testcase directly maps to AC2 | SCM-002 | AC2 | Low |
| TP_SCM2_012 | Direct | Testcase directly maps to AC4 | SCM-002 | AC4 | Low |
| TP_SCM2_013 | Direct | Testcase directly maps to AC5 | SCM-002 | AC5 | Low |
| TP_SCM2_014 | Direct | Testcase directly maps to AC1 | SCM-002 | AC1 | Low |
| TP_SCM2_015 | Direct | Testcase directly maps to AC5 | SCM-002 | AC5 | Low |
| TP_SCM3_001 | Direct | Testcase directly maps to AC1 | SCM-003 | AC1 | Low |
| TP_SCM3_002 | Direct | Testcase directly maps to AC1 | SCM-003 | AC1 | Low |
| TP_SCM3_003 | Direct | Testcase directly maps to AC2 | SCM-003 | AC2 | Low |
| TP_SCM3_004 | Direct | Testcase directly maps to AC2 | SCM-003 | AC2 | High |
| TP_SCM3_005 | Direct | Testcase directly maps to AC2 | SCM-003 | AC2 | Low |
| TP_SCM3_006 | Direct | Testcase directly maps to AC3 | SCM-003 | AC3 | Low |
| TP_SCM3_007 | Direct | Testcase directly maps to AC3 | SCM-003 | AC3 | Low |
| TP_SCM3_008 | Direct | Testcase directly maps to AC4 | SCM-003 | AC4 | Low |
| TP_SCM3_009 | Direct | Testcase directly maps to AC5 | SCM-003 | AC5 | High |
| TP_SCM3_010 | Direct | Testcase directly maps to AC1 | SCM-003 | AC1 | Low |
| TP_SCM3_011 | Direct | Testcase directly maps to AC2 | SCM-003 | AC2 | Low |
| TP_SCM3_012 | Direct | Testcase directly maps to AC4 | SCM-003 | AC4 | Low |
| TP_SCM3_013 | Direct | Testcase directly maps to AC5 | SCM-003 | AC5 | Low |
| TP_SCM4_001 | Direct | Testcase directly maps to AC1 | SCM-004 | AC1 | Low |
| TP_SCM4_002 | Direct | Testcase directly maps to AC1 | SCM-004 | AC1 | Low |
| TP_SCM4_003 | Direct | Testcase directly maps to AC2 | SCM-004 | AC2 | Low |
| TP_SCM4_004 | Direct | Testcase directly maps to AC2 | SCM-004 | AC2 | High |
| TP_SCM4_005 | Direct | Testcase directly maps to AC2 | SCM-004 | AC2 | Low |
| TP_SCM4_006 | Direct | Testcase directly maps to AC3 | SCM-004 | AC3 | Low |
| TP_SCM4_007 | Direct | Testcase directly maps to AC3 | SCM-004 | AC3 | Low |
| TP_SCM4_008 | Direct | Testcase directly maps to AC4 | SCM-004 | AC4 | Low |
| TP_SCM4_009 | Direct | Testcase directly maps to AC5 | SCM-004 | AC5 | High |
| TP_SCM4_010 | Direct | Testcase directly maps to AC1 | SCM-004 | AC1 | Low |
| TP_SCM4_011 | Direct | Testcase directly maps to AC2 | SCM-004 | AC2 | Low |
| TP_SCM4_012 | Direct | Testcase directly maps to AC4 | SCM-004 | AC4 | Low |
| TP_SCM4_013 | Direct | Testcase directly maps to AC5 | SCM-004 | AC5 | Low |
| TP_SCM5_001 | Direct | Testcase directly maps to AC1 | SCM-005 | AC1 | Low |
| TP_SCM5_002 | Direct | Testcase directly maps to AC1 | SCM-005 | AC1 | Low |
| TP_SCM5_003 | Direct | Testcase directly maps to AC1 | SCM-005 | AC1 | Low |
| TP_SCM5_004 | Direct | Testcase directly maps to AC2 | SCM-005 | AC2 | Low |
| TP_SCM5_005 | Direct | Testcase directly maps to AC2 | SCM-005 | AC2 | High |
| TP_SCM5_006 | Direct | Testcase directly maps to AC2 | SCM-005 | AC2 | Low |
| TP_SCM5_007 | Direct | Testcase directly maps to AC3 | SCM-005 | AC3 | Low |
| TP_SCM5_008 | Direct | Testcase directly maps to AC3 | SCM-005 | AC3 | Low |
| TP_SCM5_009 | Direct | Testcase directly maps to AC3 | SCM-005 | AC3 | Low |
| TP_SCM5_010 | Direct | Testcase directly maps to AC4 | SCM-005 | AC4 | Low |
| TP_SCM5_011 | Direct | Testcase directly maps to AC1 | SCM-005 | AC1 | High |
| TP_SCM5_012 | Direct | Testcase directly maps to AC2 | SCM-005 | AC2 | Low |
| TP_SCM5_013 | Direct | Testcase directly maps to AC5 | SCM-005 | AC5 | High |
| TP_SCM5_014 | Direct | Testcase directly maps to AC5 | SCM-005 | AC5 | Low |
| TP_SCM5_015 | Direct | Testcase directly maps to AC4 | SCM-005 | AC4 | High |
| TP_SCM6_001 | Direct | Testcase directly maps to AC1 | SCM-006 | AC1 | Low |
| TP_SCM6_002 | Direct | Testcase directly maps to AC1 | SCM-006 | AC1 | Low |
| TP_SCM6_003 | Direct | Testcase directly maps to AC1 | SCM-006 | AC1 | Low |
| TP_SCM6_004 | Direct | Testcase directly maps to AC2 | SCM-006 | AC2 | Low |
| TP_SCM6_005 | Direct | Testcase directly maps to AC2 | SCM-006 | AC2 | High |
| TP_SCM6_006 | Direct | Testcase directly maps to AC2 | SCM-006 | AC2 | Low |
| TP_SCM6_007 | Direct | Testcase directly maps to AC3 | SCM-006 | AC3 | Low |
| TP_SCM6_008 | Direct | Testcase directly maps to AC3 | SCM-006 | AC3 | Low |
| TP_SCM6_009 | Direct | Testcase directly maps to AC3 | SCM-006 | AC3 | Low |
| TP_SCM6_010 | Direct | Testcase directly maps to AC4 | SCM-006 | AC4 | Low |
| TP_SCM6_011 | Direct | Testcase directly maps to AC1 | SCM-006 | AC1 | Low |
| TP_SCM6_012 | Direct | Testcase directly maps to AC4 | SCM-006 | AC4 | High |
| TP_SCM6_013 | Direct | Testcase directly maps to AC5 | SCM-006 | AC5 | Low |
| TP_SCM6_014 | Direct | Testcase directly maps to AC5 | SCM-006 | AC5 | Low |
| TP_SCM6_015 | Direct | Testcase directly maps to AC5 | SCM-006 | AC5 | High |
| TP_SCM7_001 | Direct | Testcase directly maps to AC1 | SCM-007 | AC1 | Low |
| TP_SCM7_002 | Direct | Testcase directly maps to AC1 | SCM-007 | AC1 | Low |
| TP_SCM7_003 | Direct | Testcase directly maps to AC1 | SCM-007 | AC1 | Low |
| TP_SCM7_004 | Direct | Testcase directly maps to AC2 | SCM-007 | AC2 | Low |
| TP_SCM7_005 | Direct | Testcase directly maps to AC2 | SCM-007 | AC2 | High |
| TP_SCM7_006 | Direct | Testcase directly maps to AC2 | SCM-007 | AC2 | Low |
| TP_SCM7_007 | Direct | Testcase directly maps to AC3 | SCM-007 | AC3 | Low |
| TP_SCM7_008 | Direct | Testcase directly maps to AC3 | SCM-007 | AC3 | Low |
| TP_SCM7_009 | Direct | Testcase directly maps to AC3 | SCM-007 | AC3 | Low |
| TP_SCM7_010 | Direct | Testcase directly maps to AC4 | SCM-007 | AC4 | Low |
| TP_SCM7_011 | Direct | Testcase directly maps to AC1 | SCM-007 | AC1 | Low |
| TP_SCM7_012 | Direct | Testcase directly maps to AC5 | SCM-007 | AC5 | High |
| TP_SCM7_013 | Direct | Testcase directly maps to AC5 | SCM-007 | AC5 | Low |
| TP_SCM7_014 | Direct | Testcase directly maps to AC4 | SCM-007 | AC4 | High |
| TP_SCM7_015 | Direct | Testcase directly maps to AC2 | SCM-007 | AC2 | High |
| TP_SCM8_001 | Execution Mismatch | Mapped testcase ID TP_SCM8_001 has no exact matching test log testcase ID; execution log uses UT_SCM8_001 | SCM-008 | AC1 | High |
| TP_SCM8_002 | Execution Mismatch | Mapped testcase ID TP_SCM8_002 has no exact matching test log testcase ID; execution log uses UT_SCM8_002 | SCM-008 | AC1 | High |
| TP_SCM8_003 | Execution Mismatch | Mapped testcase ID TP_SCM8_003 has no exact matching test log testcase ID; execution log uses UT_SCM8_003 | SCM-008 | AC1 | High |
| TP_SCM8_004 | Execution Mismatch | Mapped testcase ID TP_SCM8_004 has no exact matching test log testcase ID; execution log uses UT_SCM8_004 | SCM-008 | AC2 | High |
| TP_SCM8_005 | Execution Mismatch | Mapped testcase ID TP_SCM8_005 has no exact matching test log testcase ID; execution log uses UT_SCM8_005 | SCM-008 | AC2 | High |
| TP_SCM8_006 | Execution Mismatch | Mapped testcase ID TP_SCM8_006 has no exact matching test log testcase ID; execution log uses UT_SCM8_006 | SCM-008 | AC3 | High |
| TP_SCM8_007 | Execution Mismatch | Mapped testcase ID TP_SCM8_007 has no exact matching test log testcase ID; execution log uses UT_SCM8_007 | SCM-008 | AC3 | High |
| TP_SCM8_008 | Execution Mismatch | Mapped testcase ID TP_SCM8_008 has no exact matching test log testcase ID; execution log uses UT_SCM8_008 | SCM-008 | AC4 | High |
| TP_SCM8_009 | Execution Mismatch | Mapped testcase ID TP_SCM8_009 has no exact matching test log testcase ID; execution log uses UT_SCM8_009 | SCM-008 | AC5 | High |
| TP_SCM8_010 | Execution Mismatch | Mapped testcase ID TP_SCM8_010 has no exact matching test log testcase ID; execution log uses UT_SCM8_010 | SCM-008 | AC1 | High |
| TP_SCM8_011 | Execution Mismatch | Mapped testcase ID TP_SCM8_011 has no exact matching test log testcase ID; execution log uses UT_SCM8_011 | SCM-008 | AC2 | High |
| TP_SCM8_012 | Execution Mismatch | Mapped testcase ID TP_SCM8_012 has no exact matching test log testcase ID; execution log uses UT_SCM8_012 | SCM-008 | AC4 | High |
| TP_SCM8_013 | Execution Mismatch | Mapped testcase ID TP_SCM8_013 has no exact matching test log testcase ID; execution log uses UT_SCM8_013 | SCM-008 | AC5 | High |
| TP_SCM8_014 | Execution Mismatch | Mapped testcase ID TP_SCM8_014 has no exact matching test log testcase ID; execution log uses UT_SCM8_014 | SCM-008 | AC2 | High |
| TP_SCM8_015 | Execution Mismatch | Mapped testcase ID TP_SCM8_015 has no exact matching test log testcase ID; execution log uses UT_SCM8_015 | SCM-008 | AC5 | High |
| UT_SCM9_001 | Direct | Testcase directly maps to AC1 | SCM-009 | AC1 | Low |
| UT_SCM9_002 | Direct | Testcase directly maps to AC1 | SCM-009 | AC1 | Low |
| UT_SCM9_003 | Direct | Testcase directly maps to AC1 | SCM-009 | AC1 | Low |
| UT_SCM9_004 | Direct | Testcase directly maps to AC2 | SCM-009 | AC2 | High |
| UT_SCM9_005 | Direct | Testcase directly maps to AC2 | SCM-009 | AC2 | Low |
| UT_SCM9_006 | Direct | Testcase directly maps to AC3 | SCM-009 | AC3 | Low |
| UT_SCM9_007 | Direct | Testcase directly maps to AC3 | SCM-009 | AC3 | Low |
| UT_SCM9_008 | Direct | Testcase directly maps to AC4 | SCM-009 | AC4 | Low |
| UT_SCM9_009 | Direct | Testcase directly maps to AC5 | SCM-009 | AC5 | Low |
| UT_SCM9_010 | Direct | Testcase directly maps to AC1 | SCM-009 | AC1 | Low |
| UT_SCM9_011 | Direct | Testcase directly maps to AC2 | SCM-009 | AC2 | Low |
| UT_SCM9_012 | Direct | Testcase directly maps to AC3 | SCM-009 | AC3 | High |
| UT_SCM9_013 | Direct | Testcase directly maps to AC5 | SCM-009 | AC5 | Low |
| UT_SCM9_014 | Direct | Testcase directly maps to AC2 | SCM-009 | AC2 | Low |
| UT_SCM9_015 | Direct | Testcase directly maps to AC5 | SCM-009 | AC5 | Low |

## Consistency Metrics Summary

| Metric | Count |
|---|---|
| total_testcases | 132 |
| total_testlogs | 130 |
| consistency_status | Inconsistent |
| missing_testlogs | 15 |
| missing_testcases | 13 |

## Defect Details

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
| DEF-SCM9-001 | UT_SCM9_004 | SCM-009 | SMS gateway timeout prevents delivery |
| DEF-SCM9-002 | UT_SCM9_012 | SCM-009 | Push notification service ignores user preference flag |

## Conclusion

Based on the provided data, at least one user story (SCM-008) has acceptance criteria with `coverage_status` = Not Covered, and multiple user stories have Partially Covered acceptance criteria and recorded defects; therefore, remediation is required before progression to ensure sufficient unit test coverage and to address the identified execution and defect issues.