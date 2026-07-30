# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 8 user stories:

- SCM-001 – Implement Order Refund Management Service  
- SCM-002 – Subscription Pause Management Service  
- SCM-003 – Subscription Upgrade Request Processing  
- SCM-004 – Subscription Cancellation Workflow  
- SCM-005 – Subscription Renewal Reminder Service  
- SCM-006 – Subscription Downgrade Management  
- SCM-007 – Subscription Transfer and Ownership Change  
- SCM-008 – Implement Customer Loyalty Points Service  

These user stories form the baseline for evaluation. The scope is restricted to:

- Unit test cases mapped to the above user stories (as represented via `mapped_testcases` in `coverage_analysis`).
- Unit test execution, test mapping consistency, and defect records as provided in the upstream JSON.

## Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-001 | AC1 | UT_SCM1_002 and UT_SCM1_003 are mapped to AC1 but do not validate all requirements for the Acceptance Criterion based on explicit artifact evidence. | Partially Covered |
| SCM-001 | AC2 | UT_SCM1_005 failed with defect evidence and UT_SCM1_011 verifies notification is NOT sent when customer contact details are absent. | Partially Covered |
| SCM-001 | AC4 | Mapped testcase UT_SCM1_008 references timestamp, but the Acceptance Criterion explicitly requires approval timestamp and no testcase explicitly validates approval timestamp; UT_SCM1_012 does not validate required fields. | Partially Covered |
| SCM-001 | AC5 | No mapped testcase explicitly validates fraud review based on artifact evidence. | Partially Covered |
| SCM-001 | AC5 | UT_SCM1_009 failed with defect evidence and UT_SCM1_015 actual result states test not yet executed. | Partially Covered |
| SCM-002 | AC1 | At least one mapped testcase for AC1 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-002 | AC1 | At least one mapped testcase for AC1 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-002 | AC1 | At least one mapped testcase for AC1 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-002 | AC2 | No mapped testcase explicitly validates resume date based on artifact evidence. | Partially Covered |
| SCM-002 | AC2 | TP_SCM2_011 verifies notification is NOT sent when customer email is missing. | Partially Covered |
| SCM-002 | AC2 | Mapped testcases do not collectively validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-002 | AC3 | No mapped testcase explicitly validates scheduled resume date based on artifact evidence. | Partially Covered |
| SCM-002 | AC4 | No mapped testcase explicitly validates pause start date in audit log based on artifact evidence. | Partially Covered |
| SCM-002 | AC4 | TP_SCM2_008 failed with defect evidence: DEF-SCM2-101 - Pause reason not captured consistently. | Partially Covered |
| SCM-002 | AC5 | TP_SCM2_009 failed with defect evidence that pause activated before approval validation, and no mapped testcase explicitly validates activation occurs only after approval. | Partially Covered |
| SCM-002 | AC5 | TP_SCM2_009 failed with defect evidence and TP_SCM2_015 actual result states test not yet executed. | Partially Covered |
| SCM-003 | AC1 | At least one mapped testcase for AC1 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-003 | AC1 | TP_SCM3_014 has no explicit execution evidence in the provided execution log artifact. | Partially Covered |
| SCM-003 | AC2 | TP_SCM3_004 failed with defect evidence: DEF-SCM3-101 - Revised billing amount not included in upgrade confirmation notification. | Partially Covered |
| SCM-003 | AC2 | TP_SCM3_011 verifies notification is NOT sent when customer email address is missing. | Partially Covered |
| SCM-003 | AC3 | No mapped testcase explicitly validates next billing cycle changes based on artifact evidence. | Partially Covered |
| SCM-003 | AC4 | At least one mapped testcase for AC4 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-003 | AC4 | At least one mapped testcase for AC4 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-003 | AC4 | At least one mapped testcase for AC4 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-003 | AC4 | At least one mapped testcase for AC4 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-003 | AC4 | At least one mapped testcase for AC4 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-003 | AC4 | At least one mapped testcase for AC4 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-003 | AC5 | No mapped testcase explicitly validates upgrade activation occurs only after approval based on artifact evidence. | Partially Covered |
| SCM-003 | AC5 | TP_SCM3_009 failed with defect evidence: DEF-SCM3-102 - Manager approval workflow not initiated when price increase equals exactly 50%. | Partially Covered |
| SCM-004 | AC1 | At least one mapped testcase for AC1 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-004 | AC1 | At least one mapped testcase for AC1 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-004 | AC1 | At least one mapped testcase for AC1 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-004 | AC2 | TP_SCM4_004 failed with defect evidence: DEF-SCM4-101 - Applicable refund details not included in cancellation confirmation notification. | Partially Covered |
| SCM-004 | AC2 | TP_SCM4_011 verifies notification is NOT sent when customer contact details are missing. | Partially Covered |
| SCM-004 | AC3 | At least one mapped testcase for AC3 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-004 | AC3 | At least one mapped testcase for AC3 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-004 | AC3 | At least one mapped testcase for AC3 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-004 | AC4 | At least one mapped testcase for AC4 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-004 | AC4 | At least one mapped testcase for AC4 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-004 | AC4 | At least one mapped testcase for AC4 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-004 | AC4 | At least one mapped testcase for AC4 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-004 | AC4 | At least one mapped testcase for AC4 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-004 | AC4 | At least one mapped testcase for AC4 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-004 | AC5 | No mapped testcase explicitly validates cancellation processing occurs only after finance team approval based on artifact evidence. | Partially Covered |
| SCM-004 | AC5 | TP_SCM4_009 failed with defect evidence and TP_SCM4_015 has no explicit execution evidence in the provided execution log artifact. | Partially Covered |
| SCM-005 | AC1 | TP_SCM5_011 failed with defect evidence: DEF-SCM5-103 - System sends reminder even when subscription expiry date is null. | Partially Covered |
| SCM-005 | AC1 | At least one mapped testcase for AC1 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-005 | AC1 | At least one mapped testcase for AC1 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-005 | AC2 | TP_SCM5_005 failed with defect evidence: DEF-SCM5-101 - Renewal amount not populated in 30-day reminder notification for monthly billing plans. | Partially Covered |
| SCM-005 | AC3 | At least one mapped testcase for AC3 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-005 | AC3 | At least one mapped testcase for AC3 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-005 | AC3 | At least one mapped testcase for AC3 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-005 | AC4 | No mapped testcase explicitly validates reminder date based on artifact evidence. | Partially Covered |
| SCM-005 | AC4 | No mapped testcase explicitly validates channel used based on artifact evidence. | Partially Covered |
| SCM-005 | AC4 | TP_SCM5_015 failed with defect evidence: DEF-SCM5-105 - Reminder log delivery status remains blank when notification channel fails. | Partially Covered |
| SCM-005 | AC5 | TP_SCM5_013 failed with defect evidence: DEF-SCM5-104 - Boundary condition error: $10,000 subscription flagged as high-value instead of requiring value >$10,000. | Partially Covered |
| SCM-005 | AC5 | No mapped testcase explicitly validates customer reminder for high-value subscriptions based on artifact evidence. | Partially Covered |
| SCM-005 | AC5 | Only below-threshold behavior is explicitly validated by TP_SCM5_014; no mapped testcase explicitly validates assigned account manager reminder for high-value subscriptions. | Partially Covered |
| SCM-006 | AC1 | At least one mapped testcase for AC1 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-006 | AC1 | At least one mapped testcase for AC1 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-006 | AC1 | At least one mapped testcase for AC1 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-006 | AC2 | TP_SCM6_005 failed with defect evidence: DEF-SCM6-101 - Adjusted billing amount not included in downgrade confirmation notification to customer. | Partially Covered |
| SCM-006 | AC3 | At least one mapped testcase for AC3 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-006 | AC3 | At least one mapped testcase for AC3 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-006 | AC3 | At least one mapped testcase for AC3 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-006 | AC4 | No mapped testcase explicitly validates previous plan based on artifact evidence. | Partially Covered |
| SCM-006 | AC4 | No mapped testcase explicitly validates downgraded plan based on artifact evidence. | Partially Covered |
| SCM-006 | AC4 | No mapped testcase explicitly validates effective date based on artifact evidence. | Partially Covered |
| SCM-006 | AC4 | TP_SCM6_012 failed with defect evidence: DEF-SCM6-102 - Audit log not created when downgrade results in zero credit amount. | Partially Covered |
| SCM-006 | AC4 | No mapped testcase explicitly validates timestamp based on artifact evidence. | Partially Covered |
| SCM-006 | AC5 | No mapped testcase explicitly validates customer retention review based on artifact evidence. | Partially Covered |
| SCM-006 | AC5 | TP_SCM6_015 failed with defect evidence: DEF-SCM6-103 - Enterprise downgrade not held pending state; processed immediately bypassing approval workflow. | Partially Covered |
| SCM-007 | AC1 | At least one mapped testcase for AC1 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-007 | AC1 | At least one mapped testcase for AC1 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-007 | AC1 | At least one mapped testcase for AC1 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-007 | AC1 | At least one mapped testcase for AC1 does not validate all requirements for the Acceptance Criterion. | Partially Covered |
| SCM-007 | AC2 | TP_SCM7_005 and TP_SCM7_015 failed with defect evidence: DEF-SCM7-101 - New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint. | Partially Covered |
| SCM-007 | AC2 | No mapped testcase explicitly validates transfer details based on artifact evidence. | Partially Covered |
| SCM-007 | AC3 | No mapped testcase explicitly validates billing change summary based on artifact evidence. | Partially Covered |
| SCM-007 | AC4 | No mapped testcase explicitly validates subscription ID based on artifact evidence. | Partially Covered |
| SCM-007 | AC4 | No mapped testcase explicitly validates transfer date based on artifact evidence. | Partially Covered |
| SCM-007 | AC4 | TP_SCM7_014 failed with defect evidence: DEF-SCM7-103 - Audit log authorization reference field empty when transfer initiated via bulk admin API. | Partially Covered |
| SCM-007 | AC4 | No mapped testcase explicitly validates timestamp based on artifact evidence. | Partially Covered |
| SCM-007 | AC5 | No mapped testcase explicitly validates billing entity change approval based on artifact evidence. | Partially Covered |
| SCM-007 | AC5 | TP_SCM7_012 failed with defect evidence: DEF-SCM7-102 - Compliance approval workflow not initiated for transfers involving tax jurisdiction change only without entity change. | Partially Covered |
| SCM-008 | AC1 | No mapped testcase IDs from the test plan have matching execution log testcase IDs in the artifact evidence for SCM-008; execution log uses UT_SCM8_* while test plan uses TP_SCM8_*. | Not Covered |
| SCM-008 | AC2 | No mapped testcase IDs from the test plan have matching execution log testcase IDs in the artifact evidence for SCM-008; execution log uses UT_SCM8_* while test plan uses TP_SCM8_*. | Not Covered |
| SCM-008 | AC3 | No mapped testcase IDs from the test plan have matching execution log testcase IDs in the artifact evidence for SCM-008; execution log uses UT_SCM8_* while test plan uses TP_SCM8_*. | Not Covered |
| SCM-008 | AC4 | No mapped testcase IDs from the test plan have matching execution log testcase IDs in the artifact evidence for SCM-008; execution log uses UT_SCM8_* while test plan uses TP_SCM8_*. | Not Covered |
| SCM-008 | AC5 | No mapped testcase IDs from the test plan have matching execution log testcase IDs in the artifact evidence for SCM-008; execution log uses UT_SCM8_* while test plan uses TP_SCM8_*. | Not Covered |

## Consistency Analysis

Per instructions, this section is populated directly from `mapping_consistency_details`. All available entries are shown.

## Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| UT_SCM1_001 | Direct | Testcase directly maps to AC1 | SCM-001 | AC1 | Low |
| UT_SCM1_002 | Direct | Testcase directly maps to AC1 | SCM-001 | AC1 | Low |
| UT_SCM1_003 | Direct | Testcase directly maps to AC1 | SCM-001 | AC1 | Low |
| UT_SCM1_004 | Direct | Testcase directly maps to AC2 | SCM-001 | AC2 | Low |
| UT_SCM1_005 | Direct | Testcase directly maps to AC2 | SCM-001 | AC2 | Medium |
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
| TP_SCM8_001 | Inconsistent Identifier | Mapped testcase ID from test plan does not have a matching testcase ID in execution log; execution log uses UT_SCM8_001 | SCM-008 | AC1 | High |
| TP_SCM8_002 | Inconsistent Identifier | Mapped testcase ID from test plan does not have a matching testcase ID in execution log; execution log uses UT_SCM8_002 | SCM-008 | AC1 | High |
| TP_SCM8_003 | Inconsistent Identifier | Mapped testcase ID from test plan does not have a matching testcase ID in execution log; execution log uses UT_SCM8_003 | SCM-008 | AC1 | High |
| TP_SCM8_004 | Inconsistent Identifier | Mapped testcase ID from test plan does not have a matching testcase ID in execution log; execution log uses UT_SCM8_004 | SCM-008 | AC2 | High |
| TP_SCM8_005 | Inconsistent Identifier | Mapped testcase ID from test plan does not have a matching testcase ID in execution log; execution log uses UT_SCM8_005 | SCM-008 | AC2 | High |
| TP_SCM8_006 | Inconsistent Identifier | Mapped testcase ID from test plan does not have a matching testcase ID in execution log; execution log uses UT_SCM8_006 | SCM-008 | AC3 | High |
| TP_SCM8_007 | Inconsistent Identifier | Mapped testcase ID from test plan does not have a matching testcase ID in execution log; execution log uses UT_SCM8_007 | SCM-008 | AC3 | High |
| TP_SCM8_008 | Inconsistent Identifier | Mapped testcase ID from test plan does not have a matching testcase ID in execution log; execution log uses UT_SCM8_008 | SCM-008 | AC4 | High |
| TP_SCM8_009 | Inconsistent Identifier | Mapped testcase ID from test plan does not have a matching testcase ID in execution log; execution log uses UT_SCM8_009 | SCM-008 | AC5 | High |
| TP_SCM8_010 | Inconsistent Identifier | Mapped testcase ID from test plan does not have a matching testcase ID in execution log; execution log uses UT_SCM8_010 | SCM-008 | AC1 | High |
| TP_SCM8_011 | Inconsistent Identifier | Mapped testcase ID from test plan does not have a matching testcase ID in execution log; execution log uses UT_SCM8_011 | SCM-008 | AC2 | High |
| TP_SCM8_012 | Inconsistent Identifier | Mapped testcase ID from test plan does not have a matching testcase ID in execution log; execution log uses UT_SCM8_012 | SCM-008 | AC4 | High |
| TP_SCM8_013 | Inconsistent Identifier | Mapped testcase ID from test plan does not have a matching testcase ID in execution log; execution log uses UT_SCM8_013 | SCM-008 | AC5 | High |
| TP_SCM8_014 | Inconsistent Identifier | Mapped testcase ID from test plan does not have a matching testcase ID in execution log; execution log uses UT_SCM8_014 | SCM-008 | AC2 | High |
| TP_SCM8_015 | Inconsistent Identifier | Mapped testcase ID from test plan does not have a matching testcase ID in execution log; execution log uses UT_SCM8_015 | SCM-008 | AC5 | High |

## Consistency Metrics Summary

| Metric | Count |
|---|---|
| total_testcases | 118 |
| total_testlogs | 116 |
| consistency_status | Inconsistent |
| missing_testlogs | 15 |
| missing_testcases | 13 |

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

## Conclusion

At least one user story (SCM-008) is Not Covered and multiple acceptance criteria across other user stories are only Partially Covered with open defects present; based on the provided data, remediation of unit test coverage, mapping consistency, and defect resolution is required before progression.
