# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report covers 19 user stories (SCM-001 to SCM-019), 95 acceptance criteria, 284 unit test cases identified in the available test plans, and 282 executable test log entries available for validation. Document completeness was largely acceptable; however, SCM-003, SCM-004, SCM-007, and SCM-008 test logs used testcase IDs that did not exactly match the corresponding test plan prefixes, SCM-003/SCM-004 logs did not contain all edge-case executions listed in the plans, and no separate defect log documents were provided, so defect details were derived from execution log defect fields only.

Derived consistency summary: total test cases = 284, total test logs = 282, missing test cases = 0.00, missing test logs = 2.00, consistency status = Partially Consistent.

## Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-001 | AC3 | Negative scenario missing. No testcase for inaccessible portal / unavailable status view. | Partially Covered |
| SCM-002 | AC2 | Resume date obligation not directly validated by any testcase. | Partially Covered |
| SCM-002 | AC3 | Scheduled resume date not directly validated by any testcase. | Partially Covered |
| SCM-002 | AC4 | Pause start date obligation not directly validated in audit log testcase. | Partially Covered |
| SCM-003 | AC3 | Next billing cycle changes not directly validated by any testcase. | Partially Covered |
| SCM-003 | AC5 | Missing execution log for edge boundary testcase TP_SCM3_015. | Fully Covered |
| SCM-004 | AC2 | Missing execution log for edge testcase TP_SCM4_014. | Fully Covered |
| SCM-004 | AC5 | Missing execution log for edge boundary testcase TP_SCM4_015. | Fully Covered |
| SCM-005 | AC4 | Channel used obligation not directly validated by any testcase. | Partially Covered |
| SCM-005 | AC5 | No positive testcase confirming both customer and assigned account manager are notified for subscriptions above $10,000. | Partially Covered |
| SCM-006 | AC4 | Previous plan, downgraded plan, effective date, credit issued, and timestamp are not comprehensively validated by available audit log testcases. | Partially Covered |
| SCM-006 | AC5 | Customer retention review obligation not directly validated by any testcase. | Partially Covered |
| SCM-007 | AC3 | Billing change summary not directly validated by any testcase. | Partially Covered |
| SCM-007 | AC4 | Subscription ID, transfer date, and timestamp are not directly validated by available audit log testcases. | Partially Covered |
| SCM-008 | AC5 | Test log testcase IDs use UT prefix while plan uses TP prefix, reducing direct traceability. | Fully Covered |

## Consistency Analysis

| Testcase ID / Reference | Consistency Type | Description | Mapped User Story ID | Mapped AC ID | Impact Level |
|---|---|---|---|---|---|
| SCM-003 log set | Missing Test Logs | Test plan defines TP_SCM3_014 and TP_SCM3_015, but execution log contains results only through TP_SCM3_013. | SCM-003 | AC1 / AC5 | Medium |
| SCM-004 log set | Missing Test Logs | Test plan defines TP_SCM4_014 and TP_SCM4_015, but execution log contains results only through TP_SCM4_013. | SCM-004 | AC2 / AC5 | Medium |
| SCM-003 testcase mapping | Direct | Testcase-to-AC mapping is explicit in the test plan and inferable in the execution log. | SCM-003 | Multiple | Low |
| SCM-004 testcase mapping | Direct | Testcase-to-AC mapping is explicit in the test plan and inferable in the execution log. | SCM-004 | Multiple | Low |
| SCM-007 testcase mapping | Ambiguous Identifier | Test plan and execution log use consistent TP IDs, but repeated defect DEF-SCM7-101 appears in two testcases for the same behavioral issue; traceability remains acceptable but defect-to-test uniqueness is reduced. | SCM-007 | AC2 | Low |
| SCM-008 testcase mapping | Ambiguous Identifier | Test plan uses TP_SCM8_xxx while execution log uses UT_SCM8_xxx for corresponding cases; AC/story mapping remains inferable. | SCM-008 | Multiple | Medium |

## Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| SCM-003 log set | Missing Test Logs | Test plan defines TP_SCM3_014 and TP_SCM3_015, but execution log contains results only through TP_SCM3_013. | SCM-003 | AC1 / AC5 | Medium |
| SCM-004 log set | Missing Test Logs | Test plan defines TP_SCM4_014 and TP_SCM4_015, but execution log contains results only through TP_SCM4_013. | SCM-004 | AC2 / AC5 | Medium |
| SCM-003 testcase mapping | Direct | Testcase-to-AC mapping is explicit in the test plan and inferable in the execution log. | SCM-003 | Multiple | Low |
| SCM-004 testcase mapping | Direct | Testcase-to-AC mapping is explicit in the test plan and inferable in the execution log. | SCM-004 | Multiple | Low |
| SCM-007 testcase mapping | Ambiguous Identifier | Test plan and execution log use consistent TP IDs, but repeated defect DEF-SCM7-101 appears in two testcases for the same behavioral issue; traceability remains acceptable but defect-to-test uniqueness is reduced. | SCM-007 | AC2 | Low |
| SCM-008 testcase mapping | Ambiguous Identifier | Test plan uses TP_SCM8_xxx while execution log uses UT_SCM8_xxx for corresponding cases; AC/story mapping remains inferable. | SCM-008 | Multiple | Medium |

## Consistency Metrics Summary

| Metric | Count |
|---|---|
| Total test cases | 284.00 |
| Total test logs | 282.00 |
| Missing test cases | 0.00 |
| Missing test logs | 2.00 |
| Consistency status | Partially Consistent |

## Defect Details

| Defect ID | Test Case ID | User Story ID | AC ID | Title / Description |
|---|---|---|---|---|
| DEF-SCM1-001 | UT_SCM1_005 | SCM-001 | AC2 | Notification template rendering issue |
| DEF-SCM1-002 | UT_SCM1_009 | SCM-001 | AC5 | Refund workflow synchronization error |
| DEF-SCM2-101 | TP_SCM2_008 | SCM-002 | AC4 | Pause reason not captured consistently |
| DEF-SCM2-102 | TP_SCM2_009 | SCM-002 | AC5 | Activation allowed without completed approval |
| DEF-SCM3-101 | TP_SCM3_004 | SCM-003 | AC2 | Revised billing amount not included in upgrade confirmation notification |
| DEF-SCM3-102 | TP_SCM3_009 | SCM-003 | AC5 | Manager approval workflow not initiated when price increase equals exactly 50% |
| DEF-SCM4-101 | TP_SCM4_004 | SCM-004 | AC2 | Applicable refund details not included in cancellation confirmation notification |
| DEF-SCM4-102 | TP_SCM4_009 | SCM-004 | AC5 | Finance team approval workflow fails for mixed currency outstanding balances |
| DEF-SCM5-101 | TP_SCM5_005 | SCM-005 | AC2 | Renewal amount not populated in 30-day reminder notification for monthly billing plans |
| DEF-SCM5-103 | TP_SCM5_011 | SCM-005 | AC1 | System sends reminder even when subscription expiry date is null |
| DEF-SCM5-104 | TP_SCM5_013 | SCM-005 | AC5 | Boundary condition error: $10,000 subscription flagged as high-value instead of requiring value >$10,000 |
| DEF-SCM5-105 | TP_SCM5_015 | SCM-005 | AC4 | Reminder log delivery status remains blank when notification channel fails |
| DEF-SCM6-101 | TP_SCM6_005 | SCM-006 | AC2 | Adjusted billing amount not included in downgrade confirmation notification to customer |
| DEF-SCM6-102 | TP_SCM6_012 | SCM-006 | AC4 | Audit log not created when downgrade results in zero credit amount |
| DEF-SCM6-103 | TP_SCM6_015 | SCM-006 | AC5 | Enterprise downgrade not held pending state; processed immediately bypassing approval workflow |
| DEF-SCM7-101 | TP_SCM7_005 | SCM-007 | AC2 | New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint |
| DEF-SCM7-102 | TP_SCM7_012 | SCM-007 | AC5 | Compliance approval workflow not initiated for transfers involving tax jurisdiction change only without entity change |
| DEF-SCM7-103 | TP_SCM7_014 | SCM-007 | AC4 | Audit log authorization reference field empty when transfer initiated via bulk admin API |
| DEF-SCM7-101 | TP_SCM7_015 | SCM-007 | AC2 | New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint |
| DEF-SCM8-001 | UT_SCM8_003 | SCM-008 | AC1 | Points posting service delay |
| DEF-SCM8-002 | UT_SCM8_007 | SCM-008 | AC3 | Balance refresh cache issue |
| DEF-SCM8-003 | UT_SCM8_009 | SCM-008 | AC5 | Redemption workflow synchronization issue |
| DEF-SCM9-001 | UT_SCM9_004 | SCM-009 | AC2 | SMS gateway timeout prevents delivery |
| DEF-SCM9-002 | UT_SCM9_012 | SCM-009 | AC3 | Push notification service ignores user preference flag |
| DEF-SCM10-001 | UT_SCM10_005 | SCM-010 | AC2 | Alert content template renders incorrect quantity field |
| DEF-SCM10-002 | UT_SCM10_009 | SCM-010 | AC5 | Approval workflow fails to trigger for bulk adjustments processed in the same batch |
| DEF-SCM11-001 | UT_SCM11_005 | SCM-011 | AC2 | Notification template does not populate requestor details field |
| DEF-SCM11-002 | UT_SCM11_009 | SCM-011 | AC5 | Director approval routing fails when requestor and approver are in different cost centers |
| DEF-SCM12-001 | UT_SCM12_005 | SCM-012 | AC2 | Notification content omits carrier name for multi-leg shipments |
| DEF-SCM12-002 | UT_SCM12_009 | SCM-012 | AC5 | Escalation event not raised when delay spans a carrier handoff |
| DEF-SCM13-001 | UT_SCM13_005 | SCM-013 | AC2 | Notification omits prior score for comparison in change summary |
| DEF-SCM13-002 | UT_SCM13_009 | SCM-013 | AC5 | Corrective action plan workflow does not trigger for suppliers with missing cost metric |
| DEF-SCM14-001 | UT_SCM14_005 | SCM-014 | AC2 | Notification fails to include picker ID for multi-picker orders |
| DEF-SCM14-002 | UT_SCM14_009 | SCM-014 | AC5 | Recount workflow does not trigger when discrepancy spans multiple SKUs on the same order |
| DEF-SCM15-001 | UT_SCM15_005 | SCM-015 | AC2 | Notification template renders incorrect item SKU for bundled returns |
| DEF-SCM15-002 | UT_SCM15_009 | SCM-015 | AC5 | QC inspection workflow fails to trigger for multi-item returns totaling above $500 |
| DEF-SCM16-001 | UT_SCM16_005 | SCM-016 | AC2 | Notification content shows stale forecast value from prior run |
| DEF-SCM16-002 | UT_SCM16_009 | SCM-016 | AC5 | Planner review workflow does not trigger when variance calculation crosses a category re-mapping |
| DEF-SCM17-001 | UT_SCM17_005 | SCM-017 | AC2 | Notification omits PO number when invoice references multiple line items |
| DEF-SCM17-002 | UT_SCM17_009 | SCM-017 | AC5 | Manager review workflow fails to trigger when discrepancy results from a currency conversion rounding difference |
| DEF-SCM18-001 | UT_SCM18_005 | SCM-018 | AC2 | Notification fails to send when SKU has an associated substitute item mapping |
| DEF-SCM18-002 | UT_SCM18_009 | SCM-018 | AC5 | Escalation workflow does not trigger when backorder is partially fulfilled before day 14 |
| DEF-SCM19-001 | UT_SCM19_005 | SCM-019 | AC2 | Notification fails to identify destination warehouse manager when transfer spans regions |
| DEF-SCM19-002 | UT_SCM19_009 | SCM-019 | AC5 | Regional manager approval workflow not triggered when transfer is split across multiple shipments |

No separate defect log documents were provided; therefore, the above table reflects all defect evidence directly extracted from the execution logs.

## Conclusion

Unit test coverage is broadly strong, but the overall quality assessment is constrained by 16 partially covered acceptance criteria, 2 missing execution log entries, and multiple open defects affecting notification content, audit completeness, and approval/escalation workflows. Remediation should prioritize closure of AC-level coverage gaps and execution evidence completion for SCM-003 and SCM-004 before considering the unit test evidence fully compliant and release-ready.
