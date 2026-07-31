# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report covers 10 user stories: SCM-010 through SCM-019. Across the reviewed source documents, 150 test cases were identified in the unit test plans and 150 corresponding execution log entries were identified in the test logs, with 0 missing test cases and 0 missing test logs; no standalone defect log documents were provided, so defect details were derived from defect references embedded in the execution logs. All reviewed user story documents contained an identifiable ID, title, and acceptance criteria, and all reviewed test plans contained explicit mappings from test cases to acceptance criteria.

The unit test scope includes subscription auto-renewal, cancellation, plan upgrade, multi-user license allocation, refund processing, trial-to-paid conversion, add-on bundling, payment method update, suspension for non-payment, and renewal price change notification. A total of 50 acceptance criteria were evaluated; based on the reviewed plans and logs, 42 acceptance criteria are Fully Covered, 8 are Partially Covered, and 0 are Not Covered.

## Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-010 | AC1 | NULL | Fully Covered |
| SCM-010 | AC2 | Defect observed in validation of plan price content for annual-billed subscriptions. | Partially Covered |
| SCM-010 | AC3 | NULL | Fully Covered |
| SCM-010 | AC4 | No testcase mapped for payment method used. No testcase mapped for renewal amount. No testcase mapped for timestamp. | Partially Covered |
| SCM-010 | AC5 | Defect observed: subscription not suspended after 3 failed retries. | Partially Covered |
| SCM-011 | AC1 | No testcase explicitly mapped for customer-initiated cancellation. Defect observed for duplicate cancellation handling in pending-cancellation state. | Partially Covered |
| SCM-011 | AC2 | NULL | Fully Covered |
| SCM-011 | AC3 | No testcase mapped for effective end date display. | Partially Covered |
| SCM-011 | AC4 | NULL | Fully Covered |
| SCM-011 | AC5 | No testcase mapped for finance team review before refund issuance. Defect observed in last-day-of-cycle proration accuracy. | Partially Covered |
| SCM-012 | AC1 | NULL | Fully Covered |
| SCM-012 | AC2 | Defect observed in last-day-of-cycle proration handling. | Partially Covered |
| SCM-012 | AC3 | Defect observed: feature access delayed at midnight billing boundary. | Partially Covered |
| SCM-012 | AC4 | No testcase mapped for prorated amount in audit log. No testcase mapped for effective date in audit log. | Partially Covered |
| SCM-012 | AC5 | NULL | Fully Covered |
| SCM-013 | AC1 | NULL | Fully Covered |
| SCM-013 | AC2 | Defect observed: graceful handling missing when revoking from member with no assigned license. | Partially Covered |
| SCM-013 | AC3 | No testcase mapped for license expiration display. | Partially Covered |
| SCM-013 | AC4 | NULL | Fully Covered |
| SCM-013 | AC5 | No testcase mapped for administrator notification of license limit. Defect observed in quick revoke/reassign count accuracy. | Partially Covered |
| SCM-014 | AC1 | NULL | Fully Covered |
| SCM-014 | AC2 | Defect observed: above-threshold refund processed before finance manager approval. | Partially Covered |
| SCM-014 | AC3 | NULL | Fully Covered |
| SCM-014 | AC4 | No testcase mapped for approver field in audit log. Defect observed: refund reason truncated for long free-text values. | Partially Covered |
| SCM-014 | AC5 | NULL | Fully Covered |
| SCM-015 | AC1 | Defect observed: expired payment method on exact trial end date follows wrong path. | Partially Covered |
| SCM-015 | AC2 | No testcase mapped for validation of specific reminder lead time. | Partially Covered |
| SCM-015 | AC3 | Defect observed: notification missing for invalid-payment-method failure path. | Partially Covered |
| SCM-015 | AC4 | NULL | Fully Covered |
| SCM-015 | AC5 | NULL | Fully Covered |
| SCM-016 | AC1 | NULL | Fully Covered |
| SCM-016 | AC2 | Defect observed: last-day add-on proration rounds to full month charge. | Partially Covered |
| SCM-016 | AC3 | No testcase mapped for total subscription cost display. | Partially Covered |
| SCM-016 | AC4 | Defect observed: rapid successive add-on actions merged into one audit entry. | Partially Covered |
| SCM-016 | AC5 | No testcase mapped for regional-regulation exception handling. | Partially Covered |
| SCM-017 | AC1 | NULL | Fully Covered |
| SCM-017 | AC2 | Defect observed: international card format incorrectly rejected. | Partially Covered |
| SCM-017 | AC3 | NULL | Fully Covered |
| SCM-017 | AC4 | No testcase mapped for old payment method reference. Defect observed: failed update attempt not logged. | Partially Covered |
| SCM-017 | AC5 | No testcase mapped for actual immediate retry using new payment method; current coverage only confirms pending retry precondition. | Partially Covered |
| SCM-018 | AC1 | Defect observed: failure counter does not reset after successful payment. | Partially Covered |
| SCM-018 | AC2 | NULL | Fully Covered |
| SCM-018 | AC3 | No testcase mapped for outstanding balance display. | Partially Covered |
| SCM-018 | AC4 | Defect observed: audit log omits failed attempts across billing cycles. | Partially Covered |
| SCM-018 | AC5 | No testcase mapped for restoration of full access within defined SLA. | Partially Covered |
| SCM-019 | AC1 | Defect observed: simultaneous tier price changes not all detected. | Partially Covered |
| SCM-019 | AC2 | No testcase mapped for validation of 30-day advance notice timing. | Partially Covered |
| SCM-019 | AC3 | NULL | Fully Covered |
| SCM-019 | AC4 | No testcase mapped for old price. No testcase mapped for new price. | Partially Covered |
| SCM-019 | AC5 | Defect observed: downgrade at effective-date boundary charged penalty in error. | Partially Covered |

## Consistency Analysis

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM10_001 to TP_SCM19_015 | Direct | All reviewed test plan entries contain explicit mapped story IDs and acceptance criteria IDs, and all reviewed execution log entries align to the same identifiers. | SCM-010 to SCM-019 | AC1 to AC5 | Low |
| TP_SCM17_010 | Partial | Test case validates existence of pending payment retry state but does not validate the AC5 obligation that updating the payment method triggers an immediate retry using the new payment method. | SCM-017 | AC5 | Medium |
| Multiple audit-log related test cases | Partial | Several audit-log acceptance criteria are only partially exercised because one or more required fields in the AC are not explicitly covered by mapped test cases. | SCM-010, SCM-012, SCM-014, SCM-017, SCM-019 | AC4 | Medium |
| TP_SCM11_001 to TP_SCM11_015 | Partial | AC coverage is incomplete where the user story obligation includes customer-initiated behavior, effective end date display, and finance review before refund issuance without direct testcase evidence. | SCM-011 | AC1, AC3, AC5 | Medium |
| TP_SCM13_006 to TP_SCM13_015, TP_SCM16_005 to TP_SCM16_014, TP_SCM18_005, TP_SCM18_013 | Partial | Portal-display acceptance criteria are partially mapped where required fields such as expiration, total subscription cost, or outstanding balance are not explicitly validated. | SCM-013, SCM-016, SCM-018 | AC3 | Medium |
| TP_SCM15_003 to TP_SCM15_015, TP_SCM19_003 to TP_SCM19_013 | Partial | Notification acceptance criteria are mapped directly, but timing obligations stated in the ACs are not explicitly validated in the test plans. | SCM-015, SCM-019 | AC2 | Medium |

## Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM10_001 to TP_SCM19_015 | Direct | All reviewed test plan entries contain explicit mapped story IDs and acceptance criteria IDs, and all reviewed execution log entries align to the same identifiers. | SCM-010 to SCM-019 | AC1 to AC5 | Low |
| TP_SCM17_010 | Partial | Test case validates existence of pending payment retry state but does not validate the AC5 obligation that updating the payment method triggers an immediate retry using the new payment method. | SCM-017 | AC5 | Medium |
| Multiple audit-log related test cases | Partial | Several audit-log acceptance criteria are only partially exercised because one or more required fields in the AC are not explicitly covered by mapped test cases. | SCM-010, SCM-012, SCM-014, SCM-017, SCM-019 | AC4 | Medium |
| TP_SCM11_001 to TP_SCM11_015 | Partial | AC coverage is incomplete where the user story obligation includes customer-initiated behavior, effective end date display, and finance review before refund issuance without direct testcase evidence. | SCM-011 | AC1, AC3, AC5 | Medium |
| TP_SCM13_006 to TP_SCM13_015, TP_SCM16_005 to TP_SCM16_014, TP_SCM18_005, TP_SCM18_013 | Partial | Portal-display acceptance criteria are partially mapped where required fields such as expiration, total subscription cost, or outstanding balance are not explicitly validated. | SCM-013, SCM-016, SCM-018 | AC3 | Medium |
| TP_SCM15_003 to TP_SCM15_015, TP_SCM19_003 to TP_SCM19_013 | Partial | Notification acceptance criteria are mapped directly, but timing obligations stated in the ACs are not explicitly validated in the test plans. | SCM-015, SCM-019 | AC2 | Medium |

## Consistency Metrics Summary

| Metric | Count |
|---|---|
| Total Test Cases | 150.00 |
| Total Test Logs | 150.00 |
| Missing Test Cases | 0.00 |
| Missing Test Logs | 0.00 |
| Consistency Status | Consistent with Partial Coverage Gaps |

## Defect Details

| Defect ID | Test Case ID | User Story ID | Defect Title | Defect Description |
|---|---|---|---|---|
| DEF-SCM10-101 | TP_SCM10_005 | SCM-010 | Reminder notification omits current plan price for annual-billed subscriptions | Reminder notification omits current plan price for annual-billed subscriptions |
| DEF-SCM10-102 | TP_SCM10_012 | SCM-010 | Subscription remains active state after 3rd failed retry instead of moving to suspended | Subscription remains active state after 3rd failed retry instead of moving to suspended |
| DEF-SCM11-101 | TP_SCM11_013 | SCM-011 | Prorated refund calculation returns small negative value for last-day-of-cycle cancellations | Prorated refund calculation returns small negative value for last-day-of-cycle cancellations |
| DEF-SCM11-102 | TP_SCM11_014 | SCM-011 | Duplicate cancellation request accepted when subscription already pending cancellation | Duplicate cancellation request accepted when subscription already pending cancellation |
| DEF-SCM12-101 | TP_SCM12_014 | SCM-012 | Feature access delayed by several minutes for upgrades processed at midnight billing boundary | Feature access delayed by several minutes for upgrades processed at midnight billing boundary |
| DEF-SCM12-102 | TP_SCM12_015 | SCM-012 | Prorated charge incorrectly applied at full price when upgrade occurs on last day of billing cycle | Prorated charge incorrectly applied at full price when upgrade occurs on last day of billing cycle |
| DEF-SCM13-101 | TP_SCM13_005 | SCM-013 | Revoking license from team member with no assignment returns generic server error instead of handled message | Revoking license from team member with no assignment returns generic server error instead of handled message |
| DEF-SCM13-102 | TP_SCM13_012 | SCM-013 | License pool count briefly shows incorrect total when revoke and reassign occur within same second | License pool count briefly shows incorrect total when revoke and reassign occur within same second |
| DEF-SCM14-101 | TP_SCM14_009 | SCM-014 | Refund reason field truncated to 50 characters in audit log for long free-text reasons | Refund reason field truncated to 50 characters in audit log for long free-text reasons |
| DEF-SCM14-102 | TP_SCM14_013 | SCM-014 | Refund request above threshold processed automatically before finance manager approval recorded | Refund request above threshold processed automatically before finance manager approval recorded |
| DEF-SCM15-101 | TP_SCM15_013 | SCM-015 | Conversion attempted using expired payment method instead of failing over to downgrade path | Conversion attempted using expired payment method instead of failing over to downgrade path |
| DEF-SCM15-102 | TP_SCM15_014 | SCM-015 | Downgrade notification not sent when conversion fails due to invalid (vs missing) payment method | Downgrade notification not sent when conversion fails due to invalid (vs missing) payment method |
| DEF-SCM16-101 | TP_SCM16_013 | SCM-016 | Prorated charge for add-on added on last day of billing cycle rounds up to full month charge | Prorated charge for add-on added on last day of billing cycle rounds up to full month charge |
| DEF-SCM16-102 | TP_SCM16_015 | SCM-016 | Audit log merges two rapid add-on actions into a single entry, losing the first action | Audit log merges two rapid add-on actions into a single entry, losing the first action |
| DEF-SCM17-101 | TP_SCM17_012 | SCM-017 | International card format with alphanumeric routing details rejected as invalid | International card format with alphanumeric routing details rejected as invalid |
| DEF-SCM17-102 | TP_SCM17_015 | SCM-017 | No audit log entry created when payment method update fails midway through processing | No audit log entry created when payment method update fails midway through processing |
| DEF-SCM18-101 | TP_SCM18_011 | SCM-018 | Consecutive failure counter does not reset after an intervening successful payment | Consecutive failure counter does not reset after an intervening successful payment |
| DEF-SCM18-102 | TP_SCM18_014 | SCM-018 | Suspension audit log omits failed attempts that occurred in a prior billing cycle | Suspension audit log omits failed attempts that occurred in a prior billing cycle |
| DEF-SCM19-101 | TP_SCM19_012 | SCM-019 | Only one of several simultaneous tier price changes is detected and flagged for notification | Only one of several simultaneous tier price changes is detected and flagged for notification |
| DEF-SCM19-102 | TP_SCM19_015 | SCM-019 | Downgrade request submitted on effective date boundary is charged a penalty fee in error | Downgrade request submitted on effective date boundary is charged a penalty fee in error |

## Conclusion

Unit test evidence demonstrates broad execution completeness and direct testcase-to-AC traceability, but overall quality is constrained by 8 partially covered acceptance criteria areas with unvalidated requirement elements and 20 logged defects affecting business-critical behaviors such as suspension, approvals, proration, audit integrity, and no-penalty handling. Remediation should prioritize closure of open defects and addition of targeted test cases for missing timing, audit-field, portal-field, approval, and retry-trigger validations before considering the tested scope fully compliant.
