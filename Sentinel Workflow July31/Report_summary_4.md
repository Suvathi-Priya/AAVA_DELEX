# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report covers 19 user stories (SCM-001 to SCM-019) derived from uploaded user story, test plan, and test log documents. A total of 285 test cases and 283 executed test log entries were identified, with 2 missing test logs for planned test cases in SCM-003 and no uploaded defect log documents; defect details were therefore derived from defect references embedded in the execution logs.

Document completeness issues noted: SCM-008 uses naming variance between user story and test artifacts but remains inferable, SCM-003 test log is missing execution evidence for TP_SCM3_014 and TP_SCM3_015, and no standalone defect log files were provided. Coverage was assessed at acceptance-criteria level across 95 ACs using test plan intent plus execution evidence.

## Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-001 | AC3 | Negative scenario missing for portal visibility/access constraint. | Partially Covered |
| SCM-002 | AC2 | Resume date required by AC not explicitly validated in test cases. | Partially Covered |
| SCM-002 | AC3 | Scheduled resume date not explicitly validated in test cases. | Partially Covered |
| SCM-002 | AC4 | Pause start date required by AC not explicitly validated in audit log testcase. | Partially Covered |
| SCM-003 | AC1 | Edge-case testcase TP_SCM3_014 has no execution log. | Partially Covered |
| SCM-003 | AC3 | Next billing cycle changes required by AC not explicitly validated in test cases. | Partially Covered |
| SCM-003 | AC5 | Boundary testcase TP_SCM3_015 has no execution log. | Partially Covered |
| SCM-005 | AC4 | Channel used required by AC not explicitly validated; only IDs and failed delivery status covered. | Partially Covered |
| SCM-006 | AC2 | Adjusted billing amount required by AC not explicitly validated. | Partially Covered |
| SCM-006 | AC4 | Previous plan, downgraded plan, effective date, credit issued, and timestamp not fully validated across mapped testcases. | Partially Covered |
| SCM-006 | AC5 | Customer retention review required by AC not explicitly validated. | Partially Covered |
| SCM-007 | AC3 | Billing change summary required by AC not explicitly validated in portal tests. | Partially Covered |
| SCM-007 | AC4 | Subscription ID, transfer date, and timestamp not explicitly validated in mapped audit tests. | Partially Covered |
| SCM-007 | AC5 | Billing entity change scenario not explicitly validated; only tax-jurisdiction-only and pending approval scenarios present. | Partially Covered |

## Consistency Analysis

| Testcase ID | Consistency Type | Description | Mapped User Story ID | Mapped Acceptance Criteria ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM3_014 | Missing Test Log | Planned testcase present in test plan but no corresponding execution result in test log. | SCM-003 | AC1 | High |
| TP_SCM3_015 | Missing Test Log | Planned testcase present in test plan but no corresponding execution result in test log. | SCM-003 | AC5 | High |
| SCM008 artifacts | Ambiguous Naming | User story file uses SCM-008 naming while test files use SCM008 naming; mapping inferable but inconsistent. | SCM-008 | NULL | Medium |
| UT_SCM8_001 to UT_SCM8_015 | ID Prefix Mismatch | Test plan uses TP_ prefix while execution log uses UT_ prefix for same mapped SCM-008 scenarios. | SCM-008 | Multiple | Medium |
| SCM-001 UT_SCM1_014 | Status Ambiguity | Status marked Passed while actual result states test not yet executed. | SCM-001 | AC2 | High |
| SCM-001 UT_SCM1_015 | Status Ambiguity | Status marked Passed while actual result states test not yet executed. | SCM-001 | AC5 | High |
| SCM-002 TP_SCM2_014 | Status Ambiguity | Status marked Passed while actual result states test not yet executed. | SCM-002 | AC1 | High |
| SCM-002 TP_SCM2_015 | Status Ambiguity | Status marked Passed while actual result states test not yet executed. | SCM-002 | AC5 | High |

## Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM3_014 | Missing Test Log | Planned testcase present in test plan but no corresponding execution result in test log. | SCM-003 | AC1 | High |
| TP_SCM3_015 | Missing Test Log | Planned testcase present in test plan but no corresponding execution result in test log. | SCM-003 | AC5 | High |
| SCM008 artifacts | Ambiguous Naming | User story file uses SCM-008 naming while test files use SCM008 naming; mapping inferable but inconsistent. | SCM-008 | NULL | Medium |
| UT_SCM8_001 to UT_SCM8_015 | ID Prefix Mismatch | Test plan uses TP_ prefix while execution log uses UT_ prefix for same mapped SCM-008 scenarios. | SCM-008 | Multiple | Medium |
| SCM-001 UT_SCM1_014 | Status Ambiguity | Status marked Passed while actual result states test not yet executed. | SCM-001 | AC2 | High |
| SCM-001 UT_SCM1_015 | Status Ambiguity | Status marked Passed while actual result states test not yet executed. | SCM-001 | AC5 | High |
| SCM-002 TP_SCM2_014 | Status Ambiguity | Status marked Passed while actual result states test not yet executed. | SCM-002 | AC1 | High |
| SCM-002 TP_SCM2_015 | Status Ambiguity | Status marked Passed while actual result states test not yet executed. | SCM-002 | AC5 | High |

## Consistency Metrics Summary

| Metric | Count |
|---|---|
| Total Test Cases | 285 |
| Total Test Logs | 283 |
| Missing Test Cases | 0 |
| Missing Test Logs | 2 |
| Consistency Status | Partially Consistent |

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
| DEF-SCM7-101 | TP_SCM7_015 | SCM-007 | New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint | New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint |
| DEF-SCM8-001 | UT_SCM8_003 | SCM-008 | Points posting service delay | Points posting service delay |
| DEF-SCM8-002 | UT_SCM8_007 | SCM-008 | Balance refresh cache issue | Balance refresh cache issue |
| DEF-SCM8-003 | UT_SCM8_009 | SCM-008 | Redemption workflow synchronization issue | Redemption workflow synchronization issue |
| DEF-SCM9-001 | UT_SCM9_004 | SCM-009 | SMS gateway timeout prevents delivery | SMS gateway timeout prevents delivery |
| DEF-SCM9-002 | UT_SCM9_012 | SCM-009 | Push notification service ignores user preference flag | Push notification service ignores user preference flag |
| DEF-SCM10-001 | UT_SCM10_005 | SCM-010 | Alert content template renders incorrect quantity field | Alert content template renders incorrect quantity field |
| DEF-SCM10-002 | UT_SCM10_009 | SCM-010 | Approval workflow fails to trigger for bulk adjustments processed in the same batch | Approval workflow fails to trigger for bulk adjustments processed in the same batch |
| DEF-SCM11-001 | UT_SCM11_005 | SCM-011 | Notification template does not populate requestor details field | Notification template does not populate requestor details field |
| DEF-SCM11-002 | UT_SCM11_009 | SCM-011 | Director approval routing fails when requestor and approver are in different cost centers | Director approval routing fails when requestor and approver are in different cost centers |
| DEF-SCM12-001 | UT_SCM12_005 | SCM-012 | Notification content omits carrier name for multi-leg shipments | Notification content omits carrier name for multi-leg shipments |
| DEF-SCM12-002 | UT_SCM12_009 | SCM-012 | Escalation event not raised when delay spans a carrier handoff | Escalation event not raised when delay spans a carrier handoff |
| DEF-SCM13-001 | UT_SCM13_005 | SCM-013 | Notification omits prior score for comparison in change summary | Notification omits prior score for comparison in change summary |
| DEF-SCM13-002 | UT_SCM13_009 | SCM-013 | Corrective action plan workflow does not trigger for suppliers with missing cost metric | Corrective action plan workflow does not trigger for suppliers with missing cost metric |
| DEF-SCM14-001 | UT_SCM14_005 | SCM-014 | Notification fails to include picker ID for multi-picker orders | Notification fails to include picker ID for multi-picker orders |
| DEF-SCM14-002 | UT_SCM14_009 | SCM-014 | Recount workflow does not trigger when discrepancy spans multiple SKUs on the same order | Recount workflow does not trigger when discrepancy spans multiple SKUs on the same order |
| DEF-SCM15-001 | UT_SCM15_005 | SCM-015 | Notification template renders incorrect item SKU for bundled returns | Notification template renders incorrect item SKU for bundled returns |
| DEF-SCM15-002 | UT_SCM15_009 | SCM-015 | QC inspection workflow fails to trigger for multi-item returns totaling above $500 | QC inspection workflow fails to trigger for multi-item returns totaling above $500 |
| DEF-SCM16-001 | UT_SCM16_005 | SCM-016 | Notification content shows stale forecast value from prior run | Notification content shows stale forecast value from prior run |
| DEF-SCM16-002 | UT_SCM16_009 | SCM-016 | Planner review workflow does not trigger when variance calculation crosses a category re-mapping | Planner review workflow does not trigger when variance calculation crosses a category re-mapping |
| DEF-SCM17-001 | UT_SCM17_005 | SCM-017 | Notification omits PO number when invoice references multiple line items | Notification omits PO number when invoice references multiple line items |
| DEF-SCM17-002 | UT_SCM17_009 | SCM-017 | Manager review workflow fails to trigger when discrepancy results from a currency conversion rounding difference | Manager review workflow fails to trigger when discrepancy results from a currency conversion rounding difference |
| DEF-SCM18-001 | UT_SCM18_005 | SCM-018 | Notification fails to send when SKU has an associated substitute item mapping | Notification fails to send when SKU has an associated substitute item mapping |
| DEF-SCM18-002 | UT_SCM18_009 | SCM-018 | Escalation workflow does not trigger when backorder is partially fulfilled before day 14 | Escalation workflow does not trigger when backorder is partially fulfilled before day 14 |
| DEF-SCM19-001 | UT_SCM19_005 | SCM-019 | Notification fails to identify destination warehouse manager when transfer spans regions | Notification fails to identify destination warehouse manager when transfer spans regions |
| DEF-SCM19-002 | UT_SCM19_009 | SCM-019 | Regional manager approval workflow not triggered when transfer is split across multiple shipments | Regional manager approval workflow not triggered when transfer is split across multiple shipments |

## Conclusion

Unit test coverage is broadly strong, but the report outcome is Partially Compliant due to 11 partially covered ACs, 2 missing execution logs, 4 status/result inconsistencies, and 44 defect instances derived from execution evidence. Remediation should prioritize correction of execution-log integrity issues and closure of approval/notification workflow defects before relying on this suite as complete unit-test evidence.
