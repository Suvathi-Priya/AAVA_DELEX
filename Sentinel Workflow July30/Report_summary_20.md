# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report covers 15 user stories (SCM-001 to SCM-015), 75 acceptance criteria, 224 documented unit test cases, and 222 corresponding test log entries derived directly from the uploaded source documents. Document completeness is partially compliant: user story, test plan, and test log files were available for 14 stories; SCM-008 used alternate file naming for plan/log and was readable, while no standalone defect log documents were provided, so defect details were derived from execution logs; two planned test cases do not have matching executed log IDs due to ID inconsistency in SCM-008, and three planned test cases/logs are missing overall because SCM-003, SCM-004, and SCM-009 each lacked one logged edge-case execution entry.

Unit test scope includes validation of functional, negative, and edge/boundary behaviors for refunds, subscription lifecycle events, notifications, inventory, procurement, logistics, supplier scoring, fulfillment, and RMA processing. Across the portfolio, every acceptance criterion has at least partial testcase coverage, with several criteria showing execution defects, incomplete boundary execution, or logging/mapping inconsistencies that affect overall quality confidence.

## Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-002 | AC2 | Resume date required by AC not explicitly validated by any testcase. | Partially Covered |
| SCM-002 | AC3 | Scheduled resume date not explicitly validated by any testcase. | Partially Covered |
| SCM-002 | AC4 | Pause start date required by AC not explicitly validated in audit log testcase; executed defect observed for pause reason capture consistency. | Partially Covered |
| SCM-003 | AC3 | Next billing cycle changes required by AC not explicitly validated by any testcase. | Partially Covered |
| SCM-003 | AC5 | Boundary testcase TP_SCM3_015 planned but no execution log found; executed defect indicates threshold handling issue. | Partially Covered |
| SCM-004 | AC5 | Boundary testcase TP_SCM4_015 planned but no execution log found; executed defect observed in finance approval workflow. | Partially Covered |
| SCM-005 | AC4 | AC requires channel used and delivery status; only IDs explicitly validated in positive audit testcase, and negative execution shows delivery status defect. | Partially Covered |
| SCM-006 | AC2 | Adjusted billing amount required by AC not explicitly validated by testcase mapping; executed defect observed in notification content. | Partially Covered |
| SCM-006 | AC4 | Previous plan, downgraded plan, effective date, credit issued, and timestamp are not all explicitly validated in testcase set; executed defect for $0 credit audit logging. | Partially Covered |
| SCM-006 | AC5 | Customer retention review required by AC not explicitly validated; executed defect shows approval gating bypass. | Partially Covered |
| SCM-007 | AC3 | Billing change summary required by AC not explicitly validated by any testcase. | Partially Covered |
| SCM-007 | AC4 | Subscription ID, transfer date, and timestamp not explicitly validated in testcase set; executed defect for authorization reference in bulk API scenario. | Partially Covered |
| SCM-009 | AC2 | Edge testcase UT_SCM9_014 planned but execution status is Pending. | Partially Covered |
| SCM-009 | AC5 | Edge testcase UT_SCM9_015 planned but execution status is Pending. | Partially Covered |

## Consistency Analysis

| Testcase ID | Consistency Type | Description | Mapped User Story ID | Mapped AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM3_015 | Missing Test Log | Planned boundary testcase present in test plan but no execution log entry found. | SCM-003 | AC5 | Medium |
| TP_SCM4_015 | Missing Test Log | Planned boundary testcase present in test plan but no execution log entry found. | SCM-004 | AC5 | Medium |
| TP_SCM8_001 to TP_SCM8_015 | Ambiguous | Test plan uses TP_ testcase IDs while execution log uses UT_ testcase IDs; mapping is inferable by sequence/AC but not explicit. | SCM-008 | AC1-AC5 | High |
| TP_SCM8_014 | Missing/Unexecuted | Planned edge testcase has no matching executed UT-prefixed completion; log shows UT_SCM8_014 Pending. | SCM-008 | AC2 | Medium |
| TP_SCM8_015 | Missing/Unexecuted | Planned boundary testcase has no matching executed UT-prefixed completion; log shows UT_SCM8_015 Pending. | SCM-008 | AC5 | Medium |
| UT_SCM9_014 | Pending Execution | Test log entry exists but execution not completed. | SCM-009 | AC2 | Medium |
| UT_SCM9_015 | Pending Execution | Test log entry exists but execution not completed. | SCM-009 | AC5 | Medium |

## Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM3_015 | Missing Test Log | Planned boundary testcase present in test plan but no execution log entry found. | SCM-003 | AC5 | Medium |
| TP_SCM4_015 | Missing Test Log | Planned boundary testcase present in test plan but no execution log entry found. | SCM-004 | AC5 | Medium |
| TP_SCM8_001 to TP_SCM8_015 | Ambiguous | Test plan uses TP_ testcase IDs while execution log uses UT_ testcase IDs; mapping is inferable by sequence/AC but not explicit. | SCM-008 | AC1-AC5 | High |
| TP_SCM8_014 | Missing/Unexecuted | Planned edge testcase has no matching executed UT-prefixed completion; log shows UT_SCM8_014 Pending. | SCM-008 | AC2 | Medium |
| TP_SCM8_015 | Missing/Unexecuted | Planned boundary testcase has no matching executed UT-prefixed completion; log shows UT_SCM8_015 Pending. | SCM-008 | AC5 | Medium |
| UT_SCM9_014 | Pending Execution | Test log entry exists but execution not completed. | SCM-009 | AC2 | Medium |
| UT_SCM9_015 | Pending Execution | Test log entry exists but execution not completed. | SCM-009 | AC5 | Medium |

## Consistency Metrics Summary

| Metric | Count |
|---|---|
| Total test cases | 224 |
| Total test logs | 222 |
| Missing test cases | 0 |
| Missing test logs | 2 |
| Pending/unexecuted logged cases | 4 |
| Consistency status | Partially Consistent |

## Defect Details

| Defect ID | Test Case ID | User Story ID | Defect Title / Description |
|---|---|---|---|
| DEF-SCM1-001 | UT_SCM1_005 | SCM-001 | Notification template rendering issue |
| DEF-SCM1-002 | UT_SCM1_009 | SCM-001 | Refund workflow synchronization error |
| DEF-SCM2-101 | TP_SCM2_008 | SCM-002 | Pause reason not captured consistently |
| DEF-SCM2-102 | TP_SCM2_009 | SCM-002 | Activation allowed without completed approval |
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
| DEF-SCM7-101 | TP_SCM7_005 | SCM-007 | New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint |
| DEF-SCM7-102 | TP_SCM7_012 | SCM-007 | Compliance approval workflow not initiated for transfers involving tax jurisdiction change only without entity change |
| DEF-SCM7-103 | TP_SCM7_014 | SCM-007 | Audit log authorization reference field empty when transfer initiated via bulk admin API |
| DEF-SCM7-101 | TP_SCM7_015 | SCM-007 | New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint |
| DEF-SCM8-001 | UT_SCM8_003 | SCM-008 | Points posting service delay |
| DEF-SCM8-002 | UT_SCM8_007 | SCM-008 | Balance refresh cache issue |
| DEF-SCM8-003 | UT_SCM8_009 | SCM-008 | Redemption workflow synchronization issue |
| DEF-SCM9-001 | UT_SCM9_004 | SCM-009 | SMS gateway timeout prevents delivery |
| DEF-SCM9-002 | UT_SCM9_012 | SCM-009 | Push notification service ignores user preference flag |
| DEF-SCM10-001 | UT_SCM10_005 | SCM-010 | Alert content template renders incorrect quantity field |
| DEF-SCM10-002 | UT_SCM10_009 | SCM-010 | Approval workflow fails to trigger for bulk adjustments processed in the same batch |
| DEF-SCM11-001 | UT_SCM11_005 | SCM-011 | Notification template does not populate requestor details field |
| DEF-SCM11-002 | UT_SCM11_009 | SCM-011 | Director approval routing fails when requestor and approver are in different cost centers |
| DEF-SCM12-001 | UT_SCM12_005 | SCM-012 | Notification content omits carrier name for multi-leg shipments |
| DEF-SCM12-002 | UT_SCM12_009 | SCM-012 | Escalation event not raised when delay spans a carrier handoff |
| DEF-SCM13-001 | UT_SCM13_005 | SCM-013 | Notification omits prior score for comparison in change summary |
| DEF-SCM13-002 | UT_SCM13_009 | SCM-013 | Corrective action plan workflow does not trigger for suppliers with missing cost metric |
| DEF-SCM14-001 | UT_SCM14_005 | SCM-014 | Notification fails to include picker ID for multi-picker orders |
| DEF-SCM14-002 | UT_SCM14_009 | SCM-014 | Recount workflow does not trigger when discrepancy spans multiple SKUs on the same order |
| DEF-SCM15-001 | UT_SCM15_005 | SCM-015 | Notification template renders incorrect item SKU for bundled returns |
| DEF-SCM15-002 | UT_SCM15_009 | SCM-015 | QC inspection workflow fails to trigger for multi-item returns totaling above $500 |

## Conclusion

Unit test coverage is broad but not fully audit-clean due to 19 partially covered acceptance criteria, 36 logged defects, 2 missing execution logs, 4 pending/unexecuted cases, and a high-impact ID mapping inconsistency in SCM-008. Remediation should prioritize closure of approval/workflow defects, completion of missing and pending boundary executions, and normalization of testcase/log identifiers before the portfolio is considered fully compliant.
