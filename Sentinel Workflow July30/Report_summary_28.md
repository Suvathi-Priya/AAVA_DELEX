# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report covers 10 user stories (SCM-010 to SCM-019), 50 acceptance criteria, 150 planned unit test cases, and 150 executed test log entries derived directly from the uploaded user story, test plan, and test log documents. All listed user story documents were readable and each contained an identifiable user story ID, title, and acceptance criteria; all test plans contained test case IDs with explicit AC mappings; all test logs contained execution results per test case; no separate defect log documents were provided, so defect details were derived from defect references embedded in the execution logs.

At aggregate level, document completeness is acceptable with 0 missing user story documents, 0 missing test plan documents, 0 missing test log documents, 0 missing test cases, and 0 missing test logs. Coverage determination was performed per AC based on documented validation intent, scenario breadth, and execution evidence, with defect impact incorporated into the final quality assessment.

## Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-010 | AC2 | Defect in notification content: current plan price omitted for annual-billed subscriptions. Timing requirement of at least 7 days prior is not explicitly validated by available test cases. | Partially Covered |
| SCM-010 | AC4 | No testcase mapped for payment method used. No testcase mapped for renewal amount. | Partially Covered |
| SCM-010 | AC5 | Defect: subscription remains active after 3 failed retries. No testcase explicitly validates retry count reaches exactly 3 before suspension. | Partially Covered |
| SCM-011 | AC1 | Defect: duplicate cancellation request accepted when subscription already pending cancellation. No testcase explicitly validates customer-initiated cancellation path. | Partially Covered |
| SCM-011 | AC3 | No testcase mapped for effective end date visibility. | Partially Covered |
| SCM-011 | AC5 | Defect: negative refund value on last-day-of-cycle cancellation. No testcase mapped for finance team review before refund issuance. | Partially Covered |
| SCM-012 | AC2 | Defect: full price applied on last day of billing cycle instead of minimal/zero proration. | Partially Covered |
| SCM-012 | AC3 | Defect: feature access delayed at midnight billing boundary; immediate access obligation not consistently met. | Partially Covered |
| SCM-012 | AC4 | No testcase mapped for prorated amount in audit log. No testcase mapped for effective date in audit log. | Partially Covered |
| SCM-013 | AC2 | Defect: graceful handling missing when revoking from user with no assigned license. | Partially Covered |
| SCM-013 | AC3 | No testcase mapped for license expiration visibility. | Partially Covered |
| SCM-013 | AC5 | Defect: license count becomes inaccurate during rapid revoke/reassign sequence. No testcase mapped for administrator notification of limit. | Partially Covered |
| SCM-014 | AC2 | Defect: above-threshold refund processed automatically before approval. | Partially Covered |
| SCM-014 | AC4 | Defect: refund reason truncated for long text. No testcase mapped for approver field in audit log. | Partially Covered |
| SCM-015 | AC1 | Defect: expired payment method on exact trial end date does not route to failure/downgrade path correctly. | Partially Covered |
| SCM-015 | AC2 | Timing requirement for specified number of days before expiration is not explicitly validated by available test cases. | Partially Covered |
| SCM-015 | AC3 | Defect: downgrade notification not sent for invalid payment method scenario. | Partially Covered |
| SCM-016 | AC2 | Defect: last-day add-on charge rounds up to full month instead of minimal proration. | Partially Covered |
| SCM-016 | AC3 | No testcase mapped for total subscription cost visibility. | Partially Covered |
| SCM-016 | AC4 | Defect: rapid add-on actions merged into single audit entry, losing first action. | Partially Covered |
| SCM-016 | AC5 | No testcase mapped for regional-regulation exception handling. | Partially Covered |
| SCM-017 | AC2 | Defect: international card format rejected as invalid. | Partially Covered |
| SCM-017 | AC4 | Defect: no audit log on failed midway update. No testcase mapped for old payment method reference. | Partially Covered |
| SCM-017 | AC5 | No testcase mapped for actual immediate retry execution using the new payment method; only pending retry precondition is validated. | Partially Covered |
| SCM-018 | AC1 | Defect: failure counter does not reset after successful payment. | Partially Covered |
| SCM-018 | AC3 | No testcase mapped for outstanding balance visibility. | Partially Covered |
| SCM-018 | AC4 | Defect: prior-cycle failed attempts omitted from audit log. | Partially Covered |
| SCM-018 | AC5 | No testcase mapped for restoration within defined SLA. | Partially Covered |
| SCM-019 | AC1 | Defect: only one of multiple simultaneous tier price changes detected. | Partially Covered |
| SCM-019 | AC2 | Timing requirement of at least 30 days in advance is not explicitly validated by available test cases. | Partially Covered |
| SCM-019 | AC4 | No testcase mapped for old price. No testcase mapped for new price. | Partially Covered |
| SCM-019 | AC5 | Defect: downgrade request at effective-date boundary incorrectly charged penalty fee. | Partially Covered |

## Consistency Analysis

| Testcase ID | Consistency Type | Description | Mapped User Story ID | Mapped AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM10_001 to TP_SCM19_015 | Direct | All test plan entries provide explicit mapping to a single user story ID and acceptance criteria ID; execution logs retain the same mappings. | SCM-010 to SCM-019 | AC1 to AC5 | Low |
| TP_SCM17_010 | Partial | Testcase validates pending retry precondition only and does not fully validate AC5 outcome of immediate retry using new payment method. | SCM-017 | AC5 | Medium |
| TP_SCM10_004 to TP_SCM10_005, TP_SCM15_003 to TP_SCM15_004, TP_SCM19_003 to TP_SCM19_005 | Partial | Notification content is mapped, but timing obligations in the related ACs are not explicitly validated by testcase design. | SCM-010 / SCM-015 / SCM-019 | AC2 / AC2 / AC2 | Medium |
| Multiple AC audit-log cases | Partial | Several audit-log ACs are explicitly mapped but do not cover all required audit fields defined in the user story acceptance criteria. | SCM-010 / SCM-012 / SCM-014 / SCM-017 / SCM-018 / SCM-019 | AC4 | Medium |

## Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM10_001 to TP_SCM19_015 | Direct | All test plan entries provide explicit mapping to a single user story ID and acceptance criteria ID; execution logs retain the same mappings. | SCM-010 to SCM-019 | AC1 to AC5 | Low |
| TP_SCM17_010 | Partial | Testcase validates pending retry precondition only and does not fully validate AC5 outcome of immediate retry using new payment method. | SCM-017 | AC5 | Medium |
| TP_SCM10_004 to TP_SCM10_005, TP_SCM15_003 to TP_SCM15_004, TP_SCM19_003 to TP_SCM19_005 | Partial | Notification content is mapped, but timing obligations in the related ACs are not explicitly validated by testcase design. | SCM-010 / SCM-015 / SCM-019 | AC2 / AC2 / AC2 | Medium |
| Multiple AC audit-log cases | Partial | Several audit-log ACs are explicitly mapped but do not cover all required audit fields defined in the user story acceptance criteria. | SCM-010 / SCM-012 / SCM-014 / SCM-017 / SCM-018 / SCM-019 | AC4 | Medium |

## Consistency Metrics Summary

| Metric | Count |
|---|---|
| Total test cases | 150 |
| Total test logs | 150 |
| Missing test cases | 0 |
| Missing test logs | 0 |
| Consistency status | Consistent with partial validation gaps |
| Duplicate mappings detected | 0 |
| Ambiguous mappings detected | 0 |
| Incomplete requirement-to-test validation mappings detected | 10 AC groups with partial obligation coverage |

## Defect Details

| Defect ID | Test Case ID | User Story ID | Defect Title / Description |
|---|---|---|---|
| DEF-SCM10-101 | TP_SCM10_005 | SCM-010 | Reminder notification omits current plan price for annual-billed subscriptions |
| DEF-SCM10-102 | TP_SCM10_012 | SCM-010 | Subscription remains active state after 3rd failed retry instead of moving to suspended |
| DEF-SCM11-101 | TP_SCM11_013 | SCM-011 | Prorated refund calculation returns small negative value for last-day-of-cycle cancellations |
| DEF-SCM11-102 | TP_SCM11_014 | SCM-011 | Duplicate cancellation request accepted when subscription already pending cancellation |
| DEF-SCM12-101 | TP_SCM12_014 | SCM-012 | Feature access delayed by several minutes for upgrades processed at midnight billing boundary |
| DEF-SCM12-102 | TP_SCM12_015 | SCM-012 | Prorated charge incorrectly applied at full price when upgrade occurs on last day of billing cycle |
| DEF-SCM13-101 | TP_SCM13_005 | SCM-013 | Revoking license from team member with no assignment returns generic server error instead of handled message |
| DEF-SCM13-102 | TP_SCM13_012 | SCM-013 | License pool count briefly shows incorrect total when revoke and reassign occur within same second |
| DEF-SCM14-101 | TP_SCM14_009 | SCM-014 | Refund reason field truncated to 50 characters in audit log for long free-text reasons |
| DEF-SCM14-102 | TP_SCM14_013 | SCM-014 | Refund request above threshold processed automatically before finance manager approval recorded |
| DEF-SCM15-101 | TP_SCM15_013 | SCM-015 | Conversion attempted using expired payment method instead of failing over to downgrade path |
| DEF-SCM15-102 | TP_SCM15_014 | SCM-015 | Downgrade notification not sent when conversion fails due to invalid (vs missing) payment method |
| DEF-SCM16-101 | TP_SCM16_013 | SCM-016 | Prorated charge for add-on added on last day of billing cycle rounds up to full month charge |
| DEF-SCM16-102 | TP_SCM16_015 | SCM-016 | Audit log merges two rapid add-on actions into a single entry, losing the first action |
| DEF-SCM17-101 | TP_SCM17_012 | SCM-017 | International card format with alphanumeric routing details rejected as invalid |
| DEF-SCM17-102 | TP_SCM17_015 | SCM-017 | No audit log entry created when payment method update fails midway through processing |
| DEF-SCM18-101 | TP_SCM18_011 | SCM-018 | Consecutive failure counter does not reset after an intervening successful payment |
| DEF-SCM18-102 | TP_SCM18_014 | SCM-018 | Suspension audit log omits failed attempts that occurred in a prior billing cycle |
| DEF-SCM19-101 | TP_SCM19_012 | SCM-019 | Only one of several simultaneous tier price changes is detected and flagged for notification |
| DEF-SCM19-102 | TP_SCM19_015 | SCM-019 | Downgrade request submitted on effective date boundary is charged a penalty fee in error |

Total defects derived from execution logs: 20.

## Conclusion

Unit test execution evidence demonstrates complete testcase-to-log traceability, but overall quality is constrained by 30 partially covered acceptance criteria and 20 logged defects, with the main remediation needs centered on timing validations, complete audit-field verification, boundary-condition handling, and unresolved functional failures. Release readiness should be considered conditional on fixing the identified defects and expanding testcase design to close the documented AC coverage gaps.
