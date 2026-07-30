# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report covers 15 user stories (SCM-001 to SCM-015), 75 acceptance criteria, 224 identified test cases, and 221 available test log entries derived from the uploaded source documents.

Document completeness review indicates that user story, test plan, and test log files were readable for all stories; however, no separate defect log documents were provided, so defect details were derived from defect references embedded in the execution logs. One planned test case in SCM-003 (TP_SCM3_015), two planned test cases in SCM-004 (TP_SCM4_014, TP_SCM4_015), and no other missing plan-to-log gaps were identified; SCM-008 also shows testcase ID inconsistency between plan IDs (TP_SCM8_xxx) and execution IDs (UT_SCM8_xxx), though acceptance-criteria/story mapping remains inferable.

## Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-002 | AC2 | Resume date not explicitly validated by any testcase. | Partially Covered |
| SCM-002 | AC3 | Scheduled resume date visibility not explicitly validated by any testcase. | Partially Covered |
| SCM-002 | AC4 | Pause start date not explicitly validated in audit log testcase. | Partially Covered |
| SCM-003 | AC3 | Next billing cycle changes not explicitly validated by any testcase. | Partially Covered |
| SCM-003 | AC5 | Boundary testcase TP_SCM3_015 missing from execution log; requirement wording is '> 50%' while plan includes exactly 50% boundary, creating ambiguity. | Partially Covered |
| SCM-004 | AC2 | Edge testcase for $0.00 refund notification missing from execution log. | Partially Covered |
| SCM-004 | AC5 | Boundary testcase for exactly $500 missing from execution log; finance approval behavior at threshold remains unexecuted. | Partially Covered |
| SCM-005 | AC4 | Reminder date and channel used are not explicitly validated by any testcase. | Partially Covered |
| SCM-005 | AC5 | No positive testcase explicitly validates both recipients for >$10,000 subscriptions; only below-threshold and exact-$10,000 behavior are covered. | Partially Covered |
| SCM-006 | AC4 | Audit testcase explicitly validates only customer/subscription IDs and $0 credit edge case; previous plan, downgraded plan, effective date, and timestamp are not fully evidenced. | Partially Covered |
| SCM-006 | AC5 | No testcase explicitly validates customer retention review component. | Partially Covered |
| SCM-007 | AC3 | Billing change summary not explicitly validated by any testcase. | Partially Covered |
| SCM-007 | AC4 | Subscription ID, transfer date, and timestamp are not explicitly validated in audit log testcases. | Partially Covered |
| SCM-010 | AC5 | Reason code requirement not explicitly validated by any testcase. | Partially Covered |
| SCM-011 | AC5 | Budget verification requirement not explicitly validated by any testcase. | Partially Covered |
| SCM-012 | AC5 | Root-cause review component not explicitly validated by any testcase. | Partially Covered |
| SCM-013 | AC5 | Quarterly business review requirement not explicitly validated by any testcase. | Partially Covered |
| SCM-014 | AC5 | Reason code requirement not explicitly validated by any testcase. | Partially Covered |

## Consistency Analysis

| Testcase ID | Consistency Type | Description | Mapped User Story ID | Mapped AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM3_015 | Missing Test Log | Planned testcase present in test plan but no execution result found in test log. | SCM-003 | AC5 | Medium |
| TP_SCM4_014 | Missing Test Log | Planned testcase present in test plan but no execution result found in test log. | SCM-004 | AC2 | Medium |
| TP_SCM4_015 | Missing Test Log | Planned testcase present in test plan but no execution result found in test log. | SCM-004 | AC5 | Medium |
| SCM-008 all cases | Ambiguous / Identifier Mismatch | Test plan uses TP_SCM8_xxx IDs while execution log uses UT_SCM8_xxx IDs; mapping is inferable by sequence and AC alignment but not directly identical. | SCM-008 | Multiple | Medium |
| TP_SCM2_008 | Partial Requirement Mapping | Audit testcase maps to AC4 but does not explicitly validate pause start date. | SCM-002 | AC4 | Low |
| TP_SCM2_006 / TP_SCM2_007 | Partial Requirement Mapping | AC3 requires scheduled resume date in portal; mapped testcases cover status and history only. | SCM-002 | AC3 | Low |
| TP_SCM2_004 / TP_SCM2_005 | Partial Requirement Mapping | AC2 requires resume date in notification; mapped testcases cover send event and pause start date only. | SCM-002 | AC2 | Low |
| TP_SCM5_010 / TP_SCM5_015 | Partial Requirement Mapping | AC4 requires reminder date and channel used; mapped tests emphasize IDs and failed delivery status. | SCM-005 | AC4 | Low |
| TP_SCM5_013 / TP_SCM5_014 | Partial Requirement Mapping | AC5 requires both customer and account manager reminder for >$10,000; positive dual-recipient validation is absent. | SCM-005 | AC5 | Medium |
| TP_SCM6_010 / TP_SCM6_012 | Partial Requirement Mapping | AC4 audit requirement includes plan details, effective date, credit, and timestamp; tests only partially evidence fields. | SCM-006 | AC4 | Low |
| TP_SCM6_013 / TP_SCM6_014 / TP_SCM6_015 | Partial Requirement Mapping | AC5 includes retention review in addition to approval; retention review is not explicitly tested. | SCM-006 | AC5 | Medium |
| TP_SCM7_007 / TP_SCM7_008 / TP_SCM7_009 | Partial Requirement Mapping | AC3 includes billing change summary; mapped tests cover status/history only. | SCM-007 | AC3 | Low |
| TP_SCM7_010 / TP_SCM7_014 | Partial Requirement Mapping | AC4 requires subscription ID, transfer date, authorization reference, and timestamp; tests only partially cover fields. | SCM-007 | AC4 | Medium |
| UT_SCM10_009 / UT_SCM10_013 / UT_SCM10_015 | Partial Requirement Mapping | AC5 requires supervisor approval and reason code; reason code validation absent. | SCM-010 | AC5 | Medium |
| UT_SCM11_009 / UT_SCM11_013 / UT_SCM11_015 | Partial Requirement Mapping | AC5 requires director approval and budget verification; budget verification not explicitly tested. | SCM-011 | AC5 | Medium |
| UT_SCM12_009 / UT_SCM12_013 / UT_SCM12_015 | Partial Requirement Mapping | AC5 requires escalation and root-cause review; root-cause review not explicitly tested. | SCM-012 | AC5 | Medium |
| UT_SCM13_009 / UT_SCM13_013 / UT_SCM13_015 | Partial Requirement Mapping | AC5 requires corrective action plan and quarterly business review; QBR not explicitly tested. | SCM-013 | AC5 | Medium |
| UT_SCM14_009 / UT_SCM14_013 / UT_SCM14_015 | Partial Requirement Mapping | AC5 requires supervisor recount and reason code; reason code validation absent. | SCM-014 | AC5 | Medium |

## Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM3_015 | Missing Test Log | Planned testcase present in test plan but no execution result found in test log. | SCM-003 | AC5 | Medium |
| TP_SCM4_014 | Missing Test Log | Planned testcase present in test plan but no execution result found in test log. | SCM-004 | AC2 | Medium |
| TP_SCM4_015 | Missing Test Log | Planned testcase present in test plan but no execution result found in test log. | SCM-004 | AC5 | Medium |
| SCM-008 all cases | Ambiguous / Identifier Mismatch | Test plan uses TP_SCM8_xxx IDs while execution log uses UT_SCM8_xxx IDs; mapping is inferable by sequence and AC alignment but not directly identical. | SCM-008 | Multiple | Medium |
| TP_SCM2_008 | Partial Requirement Mapping | Audit testcase maps to AC4 but does not explicitly validate pause start date. | SCM-002 | AC4 | Low |
| TP_SCM2_006 / TP_SCM2_007 | Partial Requirement Mapping | AC3 requires scheduled resume date in portal; mapped testcases cover status and history only. | SCM-002 | AC3 | Low |
| TP_SCM2_004 / TP_SCM2_005 | Partial Requirement Mapping | AC2 requires resume date in notification; mapped testcases cover send event and pause start date only. | SCM-002 | AC2 | Low |
| TP_SCM5_010 / TP_SCM5_015 | Partial Requirement Mapping | AC4 requires reminder date and channel used; mapped tests emphasize IDs and failed delivery status. | SCM-005 | AC4 | Low |
| TP_SCM5_013 / TP_SCM5_014 | Partial Requirement Mapping | AC5 requires both customer and account manager reminder for >$10,000; positive dual-recipient validation is absent. | SCM-005 | AC5 | Medium |
| TP_SCM6_010 / TP_SCM6_012 | Partial Requirement Mapping | AC4 audit requirement includes plan details, effective date, credit, and timestamp; tests only partially evidence fields. | SCM-006 | AC4 | Low |
| TP_SCM6_013 / TP_SCM6_014 / TP_SCM6_015 | Partial Requirement Mapping | AC5 includes retention review in addition to approval; retention review is not explicitly tested. | SCM-006 | AC5 | Medium |
| TP_SCM7_007 / TP_SCM7_008 / TP_SCM7_009 | Partial Requirement Mapping | AC3 includes billing change summary; mapped tests cover status/history only. | SCM-007 | AC3 | Low |
| TP_SCM7_010 / TP_SCM7_014 | Partial Requirement Mapping | AC4 requires subscription ID, transfer date, authorization reference, and timestamp; tests only partially cover fields. | SCM-007 | AC4 | Medium |
| UT_SCM10_009 / UT_SCM10_013 / UT_SCM10_015 | Partial Requirement Mapping | AC5 requires supervisor approval and reason code; reason code validation absent. | SCM-010 | AC5 | Medium |
| UT_SCM11_009 / UT_SCM11_013 / UT_SCM11_015 | Partial Requirement Mapping | AC5 requires director approval and budget verification; budget verification not explicitly tested. | SCM-011 | AC5 | Medium |
| UT_SCM12_009 / UT_SCM12_013 / UT_SCM12_015 | Partial Requirement Mapping | AC5 requires escalation and root-cause review; root-cause review not explicitly tested. | SCM-012 | AC5 | Medium |
| UT_SCM13_009 / UT_SCM13_013 / UT_SCM13_015 | Partial Requirement Mapping | AC5 requires corrective action plan and quarterly business review; QBR not explicitly tested. | SCM-013 | AC5 | Medium |
| UT_SCM14_009 / UT_SCM14_013 / UT_SCM14_015 | Partial Requirement Mapping | AC5 requires supervisor recount and reason code; reason code validation absent. | SCM-014 | AC5 | Medium |

## Consistency Metrics Summary

| Metric | Count |
|---|---|
| Total test cases identified | 224 |
| Total test logs identified | 221 |
| Missing test cases | 0.00 |
| Missing test logs | 3.00 |
| Consistency status | Partially Consistent due to 3 missing execution records, 1 story-level testcase ID mismatch set, and multiple partial requirement-to-test mappings where obligation elements were not explicitly validated. |

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

Unit test coverage is broadly strong, but the overall quality status is Partially Acceptable because 12 acceptance criteria are only partially covered, 3 planned tests have no execution evidence, and multiple defects remain open against notification, approval, audit, and boundary-condition behaviors. Remediation should prioritize executing missing test logs, adding explicit tests for unvalidated obligation components such as fraud review, resume date, reason code, root-cause/QBR/budget verification, and resolving the logged defects before release sign-off.
