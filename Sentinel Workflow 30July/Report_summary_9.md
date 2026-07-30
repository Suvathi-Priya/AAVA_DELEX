# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 7 user stories:

- SCM-001 – Implement Order Refund Management Service  
- SCM-002 – Subscription Pause Management Service  
- SCM-003 – Subscription Upgrade Request Processing  
- SCM-004 – Subscription Cancellation Workflow  
- SCM-005 – Subscription Renewal Reminder Service  
- SCM-006 – Subscription Downgrade Management  
- SCM-007 – Subscription Transfer and Ownership Change  

These user stories form the baseline for evaluation. The scope is restricted to unit test plans, mapped unit test cases, execution/consistency records, and defect details as provided in the upstream JSON.

## Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-001 | AC1 | UT_SCM1_002, UT_SCM1_003, and UT_SCM1_010 do not validate all requirements for AC1 based on explicit artifact evidence. | Partially Covered |
| SCM-001 | AC2 | UT_SCM1_005 failed with DEF-SCM1-001 - Notification template rendering issue; UT_SCM1_011 does not validate sending notification because expected result is Notification skipped; error logged; refund process continues. | Partially Covered |
| SCM-001 | AC4 | UT_SCM1_012 does not validate required audit log fields; expected result is Single audit log entry; idempotency enforced. | Partially Covered |
| SCM-001 | AC5 | UT_SCM1_009 failed with DEF-SCM1-002 - Refund workflow synchronization error; UT_SCM1_013 validates below-threshold behavior only.; No mapped testcase explicitly validates fraud review for high-value refunds above $1000 in the provided artifacts. | Partially Covered |
| SCM-002 | AC1 | TP_SCM2_010 and TP_SCM2_014 do not validate all requirements for AC1 based on explicit artifact evidence. | Partially Covered |
| SCM-002 | AC2 | TP_SCM2_011 does not validate sending notifications because expected result is Notification skipped; error logged; pause still recorded.; TP_SCM2_011 does not validate notification content because expected result is Notification skipped; error logged; pause still recorded.; No mapped testcase explicitly validates inclusion of resume date in pause confirmation notifications in the provided artifacts. | Partially Covered |
| SCM-002 | AC3 | No mapped testcase explicitly validates scheduled resume date visibility in the customer portal in the provided artifacts. | Partially Covered |
| SCM-002 | AC4 | TP_SCM2_008 failed with DEF-SCM2-101 - Pause reason not captured consistently; no testcase explicitly validates all required audit log fields successfully.; TP_SCM2_008 failed with DEF-SCM2-101 - Pause reason not captured consistently; TP_SCM2_012 validates cancelled pause event capture only.; TP_SCM2_008 failed with DEF-SCM2-101 - Pause reason not captured consistently.; No mapped testcase explicitly validates capture of pause start date in pause audit logs in the provided artifacts.; TP_SCM2_008 failed with DEF-SCM2-101 - Pause reason not captured consistently; no testcase explicitly validates all required audit log fields successfully. | Not Covered |
| SCM-002 | AC5 | TP_SCM2_009 failed with DEF-SCM2-102 - Activation allowed without completed approval; TP_SCM2_013 validates below-threshold behavior only. | Partially Covered |
| SCM-003 | AC1 | TP_SCM3_010 does not validate submission requirement because expected result is Error returned; same-plan upgrade not permitted.; TP_SCM3_010 does not validate target plan capture because expected result is Error returned; same-plan upgrade not permitted.; TP_SCM3_010 does not validate preferred upgrade date capture because expected result is Error returned; same-plan upgrade not permitted. | Partially Covered |
| SCM-003 | AC2 | TP_SCM3_004 failed with DEF-SCM3-101 - Revised billing amount not included in upgrade confirmation notification; no other testcase explicitly validates new plan details.; TP_SCM3_004 failed with DEF-SCM3-101 - Revised billing amount not included in upgrade confirmation notification; no other testcase explicitly validates effective date content.; TP_SCM3_004 failed with DEF-SCM3-101 - Revised billing amount not included in upgrade confirmation notification. | Partially Covered |
| SCM-003 | AC3 | No mapped testcase explicitly validates next billing cycle changes visibility in the customer portal in the provided artifacts. | Partially Covered |
| SCM-003 | AC4 | TP_SCM3_012 does not validate required audit log fields; expected result is Single audit entry; idempotency enforced. | Partially Covered |
| SCM-003 | AC5 | TP_SCM3_009 failed with DEF-SCM3-102 - Manager approval workflow not initiated when price increase equals exactly 50%; TP_SCM3_013 validates below-threshold behavior only; no successful mapped testcase validates the stated requirement. | Not Covered |
| SCM-004 | AC1 | TP_SCM4_010 does not validate submission requirement because expected result is Empty reason rejected with validation error.; TP_SCM4_010 does not validate cancellation reason capture because expected result is Empty reason rejected with validation error.; TP_SCM4_010 does not validate cancellation date capture because expected result is Empty reason rejected with validation error. | Partially Covered |
| SCM-004 | AC2 | TP_SCM4_004 failed with DEF-SCM4-101 - Applicable refund details not included in cancellation confirmation notification; no other testcase explicitly validates effective cancellation date inclusion.; TP_SCM4_004 failed with DEF-SCM4-101 - Applicable refund details not included in cancellation confirmation notification. | Partially Covered |
| SCM-004 | AC3 | TP_SCM4_007 validates refund status and service end date only.; TP_SCM4_006 validates cancellation status only.; TP_SCM4_006 validates cancellation status only. | Partially Covered |
| SCM-004 | AC4 | TP_SCM4_012 does not validate required audit log fields; expected result is Reversal event captured; original record preserved. | Partially Covered |
| SCM-004 | AC5 | TP_SCM4_009 failed with DEF-SCM4-102 - Finance team approval workflow fails for mixed currency outstanding balances; TP_SCM4_013 validates below-threshold behavior only. | Partially Covered |
| SCM-005 | AC1 | TP_SCM5_011 failed with DEF-SCM5-103 - System sends reminder even when subscription expiry date is null.; TP_SCM5_011 failed with DEF-SCM5-103 - System sends reminder even when subscription expiry date is null.; TP_SCM5_011 failed with DEF-SCM5-103 - System sends reminder even when subscription expiry date is null. | Partially Covered |
| SCM-005 | AC2 | TP_SCM5_005 failed with DEF-SCM5-101 - Renewal amount not populated in 30-day reminder notification for monthly billing plans. | Partially Covered |
| SCM-005 | AC3 | TP_SCM5_008 and TP_SCM5_009 do not validate upcoming renewal schedules based on explicit artifact evidence.; TP_SCM5_007 and TP_SCM5_009 do not validate reminder history based on explicit artifact evidence.; TP_SCM5_007 and TP_SCM5_008 do not validate renewal preferences based on explicit artifact evidence. | Partially Covered |
| SCM-005 | AC4 | No mapped testcase explicitly validates reminder date capture in renewal reminder logs in the provided artifacts.; No mapped testcase explicitly validates channel used capture in renewal reminder logs in the provided artifacts.; TP_SCM5_015 failed with DEF-SCM5-105 - Reminder log delivery status remains blank when notification channel fails. | Partially Covered |
| SCM-005 | AC5 | TP_SCM5_013 failed with DEF-SCM5-104 - Boundary condition error: $10,000 subscription flagged as high-value instead of requiring value >$10,000; no successful mapped testcase validates high-value identification for value greater than $10,000.; No mapped testcase explicitly validates sending reminders to the customer for high-value subscriptions in the provided artifacts.; TP_SCM5_014 validates below-threshold behavior only; no successful mapped testcase explicitly validates sending reminders to the assigned account manager for high-value subscriptions. | Not Covered |
| SCM-006 | AC1 | TP_SCM6_011 does not validate submission requirement because expected result is System rejects request with appropriate validation error.; TP_SCM6_011 does not validate target lower plan capture because expected result is System rejects request with appropriate validation error.; TP_SCM6_011 does not validate effective date capture because expected result is System rejects request with appropriate validation error.; TP_SCM6_011 does not validate lower-plan validation because expected result is System rejects request with appropriate validation error. | Partially Covered |
| SCM-006 | AC2 | TP_SCM6_005 failed with DEF-SCM6-101 - Adjusted billing amount not included in downgrade confirmation notification to customer; no other testcase explicitly validates new plan features inclusion.; TP_SCM6_005 failed with DEF-SCM6-101 - Adjusted billing amount not included in downgrade confirmation notification to customer; no other testcase explicitly validates effective date inclusion.; TP_SCM6_005 failed with DEF-SCM6-101 - Adjusted billing amount not included in downgrade confirmation notification to customer. | Partially Covered |
| SCM-006 | AC3 | TP_SCM6_008 and TP_SCM6_009 do not validate downgrade request status based on explicit artifact evidence.; TP_SCM6_007 and TP_SCM6_009 do not validate plan comparison based on explicit artifact evidence.; TP_SCM6_007 and TP_SCM6_008 do not validate credit adjustments based on explicit artifact evidence. | Partially Covered |
| SCM-006 | AC4 | No mapped testcase explicitly validates previous plan capture in downgrade audit logs in the provided artifacts.; No mapped testcase explicitly validates downgraded plan capture in downgrade audit logs in the provided artifacts.; No mapped testcase explicitly validates effective date capture in downgrade audit logs in the provided artifacts.; TP_SCM6_012 failed with DEF-SCM6-102 - Audit log not created when downgrade results in zero credit amount.; No mapped testcase explicitly validates timestamp capture in downgrade audit logs in the provided artifacts. | Partially Covered |
| SCM-006 | AC5 | TP_SCM6_015 failed with DEF-SCM6-103 - Enterprise downgrade not held pending state; processed immediately bypassing approval workflow.; No mapped testcase explicitly validates customer retention review for enterprise-tier downgrade requests in the provided artifacts. | Partially Covered |
| SCM-007 | AC1 | TP_SCM7_011 does not validate initiation requirement because expected result is System rejects transfer request with owner not found error.; TP_SCM7_011 does not validate current owner capture because expected result is System rejects transfer request with owner not found error.; TP_SCM7_011 does not validate new owner capture because expected result is System rejects transfer request with owner not found error.; TP_SCM7_011 does not validate transfer effective date capture because expected result is System rejects transfer request with owner not found error.; TP_SCM7_011 does not validate new owner eligibility because expected result is System rejects transfer request with owner not found error. | Partially Covered |
| SCM-007 | AC2 | TP_SCM7_005 failed with DEF-SCM7-101 - New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint; TP_SCM7_015 failed with DEF-SCM7-101 - New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint.; No mapped testcase explicitly validates inclusion of transfer details in transfer notification in the provided artifacts. | Partially Covered |
| SCM-007 | AC3 | No mapped testcase explicitly validates billing change summary visibility in the customer portal in the provided artifacts. | Partially Covered |
| SCM-007 | AC4 | No mapped testcase explicitly validates subscription ID capture in transfer audit logs in the provided artifacts.; No mapped testcase explicitly validates transfer date capture in transfer audit logs in the provided artifacts.; TP_SCM7_014 failed with DEF-SCM7-103 - Audit log authorization reference field empty when transfer initiated via bulk admin API.; No mapped testcase explicitly validates timestamp capture in transfer audit logs in the provided artifacts. | Partially Covered |
| SCM-007 | AC5 | TP_SCM7_012 failed with DEF-SCM7-102 - Compliance approval workflow not initiated for transfers involving tax jurisdiction change only without entity change. | Partially Covered |

## Consistency Analysis

This section is sourced strictly from `mapping_consistency_details` and `consistency_summary` from the JSON.

## Data Mapping Inconsistency Details

Per the **CONSISTENCY ANALYSIS DATA SOURCE RULE**, rows must come directly from `mapping_consistency_details`. The provided JSON `mapping_consistency_details` entries use `consistency_type` values such as `"Direct"` and describe correct mappings rather than inconsistencies, and they do not use the allowed inconsistency types `missing_testcase` or `missing_testlog`.

Because there are **no entries representing mapping inconsistencies** (and no `missing_testcase` or `missing_testlog` records), this subsection is **not displayed**, in line with the rule:

- “if `mapping_consistency_details` is empty then do not display the Data Mapping Inconsistency Details sub section”

In practical terms for this report, mapping consistency issues are not reported, and the subsection is omitted.

## Consistency Metrics Summary

| Metric | Count |
|---|---|
| Total Test Cases | 103 |
| Total Test Logs | 103 |
| Missing Test Cases | 0 |
| Missing Test Logs | 0 |
| Consistency Status | Consistent |

## Defect Details

This section is generated exclusively from:

- `coverage_analysis[*].acceptance_criteria_details[*].defect_details[*]`

No other source is used. Every defect record in those lists appears exactly once below. “Defect Description” does not repeat the defect ID text beyond what is present in the JSON description.

## Defect Details

| Defect ID | Test Case ID | User Story ID | Defect Title | Defect Description |
|---|---|---|---|---|
| DEF-SCM1-001 | UT_SCM1_005 | SCM-001 | DEF-SCM1-001 | DEF-SCM1-001 - Notification template rendering issue |
| DEF-SCM1-002 | UT_SCM1_009 | SCM-001 | DEF-SCM1-002 | DEF-SCM1-002 - Refund workflow synchronization error |
| DEF-SCM2-101 | TP_SCM2_008 | SCM-002 | DEF-SCM2-101 | DEF-SCM2-101 - Pause reason not captured consistently |
| DEF-SCM2-102 | TP_SCM2_009 | SCM-002 | DEF-SCM2-102 | DEF-SCM2-102 - Activation allowed without completed approval |
| DEF-SCM3-101 | TP_SCM3_004 | SCM-003 | DEF-SCM3-101 | DEF-SCM3-101 - Revised billing amount not included in upgrade confirmation notification |
| DEF-SCM3-102 | TP_SCM3_009 | SCM-003 | DEF-SCM3-102 | DEF-SCM3-102 - Manager approval workflow not initiated when price increase equals exactly 50% |
| DEF-SCM4-101 | TP_SCM4_004 | SCM-004 | DEF-SCM4-101 | DEF-SCM4-101 - Applicable refund details not included in cancellation confirmation notification |
| DEF-SCM4-102 | TP_SCM4_009 | SCM-004 | DEF-SCM4-102 | DEF-SCM4-102 - Finance team approval workflow fails for mixed currency outstanding balances |
| DEF-SCM5-103 | TP_SCM5_011 | SCM-005 | DEF-SCM5-103 | DEF-SCM5-103 - System sends reminder even when subscription expiry date is null |
| DEF-SCM5-101 | TP_SCM5_005 | SCM-005 | DEF-SCM5-101 | DEF-SCM5-101 - Renewal amount not populated in 30-day reminder notification for monthly billing plans |
| DEF-SCM5-105 | TP_SCM5_015 | SCM-005 | DEF-SCM5-105 | DEF-SCM5-105 - Reminder log delivery status remains blank when notification channel fails |
| DEF-SCM5-104 | TP_SCM5_013 | SCM-005 | DEF-SCM5-104 | DEF-SCM5-104 - Boundary condition error: $10,000 subscription flagged as high-value instead of requiring value >$10,000 |
| DEF-SCM6-101 | TP_SCM6_005 | SCM-006 | DEF-SCM6-101 | DEF-SCM6-101 - Adjusted billing amount not included in downgrade confirmation notification to customer |
| DEF-SCM6-102 | TP_SCM6_012 | SCM-006 | DEF-SCM6-102 | DEF-SCM6-102 - Audit log not created when downgrade results in zero credit amount |
| DEF-SCM6-103 | TP_SCM6_015 | SCM-006 | DEF-SCM6-103 | DEF-SCM6-103 - Enterprise downgrade not held pending state; processed immediately bypassing approval workflow |
| DEF-SCM7-101 | TP_SCM7_005 | SCM-007 | DEF-SCM7-101 | DEF-SCM7-101 - New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint |
| DEF-SCM7-101 | TP_SCM7_015 | SCM-007 | DEF-SCM7-101 | DEF-SCM7-101 - New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint |
| DEF-SCM7-103 | TP_SCM7_014 | SCM-007 | DEF-SCM7-103 | DEF-SCM7-103 - Audit log authorization reference field empty when transfer initiated via bulk admin API |
| DEF-SCM7-102 | TP_SCM7_012 | SCM-007 | DEF-SCM7-102 | DEF-SCM7-102 - Compliance approval workflow not initiated for transfers involving tax jurisdiction change only without entity change |

## Conclusion

Several acceptance criteria are Not Covered (for example, SCM-002/AC4, SCM-003/AC5, SCM-005/AC5), and multiple defects are recorded across the covered acceptance criteria; therefore, remediation of coverage gaps and resolution of existing defects are required before progression based on this unit test suite.
