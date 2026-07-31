# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report covers 19 user stories (SCM-001 to SCM-019) identified from the uploaded source documents. Document completeness validation indicates 19 identifiable user stories with IDs, titles, and acceptance criteria, 19 corresponding unit test plan documents with test case IDs and AC mappings, and 19 corresponding test execution log documents with execution results per test case. No standalone defect log documents were provided; defect details were derived from the defect fields embedded in the execution logs. Total derived scope includes 285 planned test cases, 285 test log entries, 0.00 missing test cases, 0.00 missing test logs, and an overall mapping consistency status of Consistent. One document gap was identified: SCM-008 test plan and test log filenames differ from the hyphenated naming pattern but remain readable and mappable; no unreadable documents were detected.

## Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-002 | AC2 | Resume date validation missing in test plan/log | Partially Covered |
| SCM-002 | AC3 | Scheduled resume date validation missing in test plan/log | Partially Covered |
| SCM-002 | AC4 | Pause start date not explicitly validated in audit log testcase | Partially Covered |
| SCM-003 | AC3 | Next billing cycle change validation missing in test plan/log | Partially Covered |
| SCM-003 | AC5 | Boundary testcase conflicts with AC wording; exact 50% scenario included though AC states greater than 50% | Partially Covered |
| SCM-004 | AC5 | Boundary testcase conflicts with AC wording; exact $500 scenario included though AC states greater than $500 | Partially Covered |
| SCM-005 | AC4 | Reminder date and channel used not explicitly validated in test plan/log | Partially Covered |
| SCM-005 | AC5 | Positive testcase validates threshold identification only; explicit dual-recipient notification to both parties missing | Partially Covered |
| SCM-006 | AC4 | Previous plan, downgraded plan, effective date, and timestamp not explicitly validated in audit log testcase | Partially Covered |
| SCM-006 | AC5 | Customer retention review validation missing in test plan/log | Partially Covered |
| SCM-007 | AC3 | Billing change summary validation missing in test plan/log | Partially Covered |
| SCM-007 | AC4 | Subscription ID, transfer date, and timestamp not explicitly validated in audit log testcase | Partially Covered |
| SCM-008 | AC5 | Fraud review validation missing in test plan/log | Partially Covered |
| SCM-010 | AC5 | Reason code validation missing in test plan/log; boundary testcase conflicts with AC wording | Partially Covered |
| SCM-011 | AC5 | Budget verification validation missing in test plan/log; boundary testcase conflicts with AC wording | Partially Covered |
| SCM-012 | AC5 | Root-cause review validation missing in test plan/log; boundary testcase conflicts with AC wording | Partially Covered |
| SCM-013 | AC5 | Quarterly business review validation missing in test plan/log; boundary testcase conflicts with AC wording | Partially Covered |
| SCM-014 | AC5 | Reason code validation missing in test plan/log | Partially Covered |
| SCM-015 | AC5 | Boundary testcase conflicts with AC wording; exact $500 scenario included though AC states above $500 | Partially Covered |
| SCM-016 | AC5 | Boundary testcase conflicts with AC wording; exact 30% scenario included though AC states above 30% | Partially Covered |
| SCM-017 | AC5 | Boundary testcase conflicts with AC wording; exact $200 scenario included though AC states above $200 | Partially Covered |
| SCM-018 | AC5 | Boundary testcase conflicts with AC wording; exact 14-day scenario included though AC states beyond 14 days | Partially Covered |
| SCM-019 | AC5 | Boundary testcase conflicts with AC wording; exact 1,000-unit scenario included though AC states above 1,000 | Partially Covered |

## Consistency Analysis

Consistency metrics summary: total test cases = 285.00, total test logs = 285.00, missing test cases = 0.00, missing test logs = 0.00, consistency status = Partially Consistent. The dataset is structurally complete, but requirement-to-test boundary mismatches and one ID/naming inconsistency reduce full mapping consistency confidence.

## Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| SCM-008 file naming set | Ambiguous Naming | Test plan and test log use `SCM008` naming while user story uses `SCM-008`; content remains consistently mapped to SCM-008 | SCM-008 | NULL | Low |
| SCM-003 AC5 boundary | Requirement/Test Boundary Mismatch | AC states approval required for price increase greater than 50%, while testcase asserts exact 50% triggers approval | SCM-003 | AC5 | Medium |
| SCM-004 AC5 boundary | Requirement/Test Boundary Mismatch | AC states outstanding balance greater than $500, while testcase asserts exact $500 triggers approval | SCM-004 | AC5 | Medium |
| SCM-010 AC5 boundary | Requirement/Test Boundary Mismatch | AC states above 500 units, while testcase asserts exact 500 triggers approval | SCM-010 | AC5 | Medium |
| SCM-011 AC5 boundary | Requirement/Test Boundary Mismatch | AC states above $10,000, while testcase asserts exact $10,000 triggers approval | SCM-011 | AC5 | Medium |
| SCM-012 AC5 boundary | Requirement/Test Boundary Mismatch | AC states delayed beyond 48 hours, while testcase asserts exactly 48 hours triggers escalation | SCM-012 | AC5 | Medium |
| SCM-013 AC5 boundary | Requirement/Test Boundary Mismatch | AC states scoring below 60, while testcase asserts exact 60 triggers corrective action | SCM-013 | AC5 | Medium |
| SCM-015 AC5 boundary | Requirement/Test Boundary Mismatch | AC states above $500, while testcase asserts exact $500 triggers inspection workflow | SCM-015 | AC5 | Medium |
| SCM-016 AC5 boundary | Requirement/Test Boundary Mismatch | AC states above 30% variance, while testcase asserts exact 30% triggers review | SCM-016 | AC5 | Medium |
| SCM-017 AC5 boundary | Requirement/Test Boundary Mismatch | AC states above $200 discrepancy, while testcase asserts exact $200 triggers review | SCM-017 | AC5 | Medium |
| SCM-018 AC5 boundary | Requirement/Test Boundary Mismatch | AC states beyond 14 days, while testcase asserts exactly 14 days triggers escalation | SCM-018 | AC5 | Medium |
| SCM-019 AC5 boundary | Requirement/Test Boundary Mismatch | AC states above 1,000 units, while testcase asserts exact 1,000 units triggers approval | SCM-019 | AC5 | Medium |
| SCM-008 execution IDs | Ambiguous Mapping | Test plan uses `TP_SCM8_xxx` IDs while execution log uses `UT_SCM8_xxx` IDs for corresponding scenarios | SCM-008 | Multiple | Medium |

## Consistency Metrics Summary

| Metric | Count |
|---|---|
| Total Test Cases | 285.00 |
| Total Test Logs | 285.00 |
| Missing Test Cases | 0.00 |
| Missing Test Logs | 0.00 |
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

Unit test evidence is structurally complete, but quality is not audit-ready for full compliance because 33.00 acceptance criteria are only partially covered and 44.00 defects were reported, with recurring gaps around missing sub-obligation validation and AC boundary-condition mismatches. Remediation should prioritize correction of failing approval/notification workflows, closure of all open defects, and alignment of test cases to exact AC threshold wording before sign-off.
