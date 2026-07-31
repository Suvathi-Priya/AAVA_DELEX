# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report covers 10 user stories (SCM-010 to SCM-019), 50 acceptance criteria, 150 planned unit test cases, and 150 executed test log entries derived directly from the uploaded user story, test plan, and test log documents.

Document completeness validation is satisfactory for all listed stories: each user story contains an identifiable ID, title, and acceptance criteria; each test plan contains test case IDs with explicit AC mapping; each test log contains execution status per test case; no separate defect log document was provided, so defect details were derived from defect references embedded in the execution logs. Overall execution outcome is 132 passed tests and 18 failed tests, with no missing test plans, no missing test logs, and no unreadable uploaded files identified from the supplied set.

## Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-010 | AC3 | Customer portal validation covers renewal date, renewal amount, and auto-renewal status, but no negative scenario for incorrect or unavailable portal data is present. | Partially Covered |
| SCM-010 | AC4 | Audit log coverage is incomplete for payment method used, renewal amount, and timestamp; only subscription ID and renewal date are directly validated. | Partially Covered |
| SCM-011 | AC3 | Cancellation status is validated, but effective end date visibility required by the AC is not directly covered by a test case. | Partially Covered |
| SCM-011 | AC5 | Prorated refund calculation is validated, but finance team review before refund issuance is not directly validated by a dedicated test case. | Partially Covered |
| SCM-012 | AC4 | Audit log coverage omits direct validation of prorated amount and effective date; previous plan, new plan, and timestamp are covered. | Partially Covered |
| SCM-013 | AC3 | Team member portal status is covered, but expiration visibility required by the AC is not directly validated. | Partially Covered |
| SCM-013 | AC5 | Assignment blocking at license limit is validated, but administrator notification of the limit is not directly validated. | Partially Covered |
| SCM-014 | AC4 | Audit log coverage does not directly validate approver capture when applicable. | Partially Covered |
| SCM-015 | AC2 | Reminder notification timing is referenced generically, but the specified number-of-days rule is not directly validated against a concrete timing threshold. | Partially Covered |
| SCM-016 | AC3 | Portal validation covers active add-ons and individual charges, but total subscription cost visibility required by the AC is not directly validated. | Partially Covered |
| SCM-016 | AC5 | Removal and no-refund behavior are covered, but regional-regulation exception handling is not directly validated. | Partially Covered |
| SCM-017 | AC4 | Audit log coverage omits direct validation of old payment method reference. | Partially Covered |
| SCM-017 | AC5 | Pending retry precondition is validated, but no test directly confirms immediate retry using the new payment method after update. | Partially Covered |
| SCM-018 | AC3 | Suspension status is validated, but outstanding balance visibility required by the AC is not directly validated. | Partially Covered |
| SCM-018 | AC5 | Reinstatement after payment is covered, but restoration of full access within a defined SLA is not directly validated. | Partially Covered |
| SCM-019 | AC2 | Notification content is covered, but the requirement to notify at least 30 days in advance is not directly validated by an explicit timing test. | Partially Covered |
| SCM-019 | AC4 | Audit log coverage does not directly validate old price and new price capture. | Partially Covered |

## Consistency Analysis

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM10_001 to TP_SCM10_015 | Direct | All SCM-010 test cases contain explicit mapping to user story SCM-010 and to a single acceptance criterion in both test plan and execution log. | SCM-010 | AC1-AC5 | Low |
| TP_SCM11_001 to TP_SCM11_015 | Direct | All SCM-011 test cases contain explicit mapping to user story SCM-011 and to a single acceptance criterion in both test plan and execution log. | SCM-011 | AC1-AC5 | Low |
| TP_SCM12_001 to TP_SCM12_015 | Direct | All SCM-012 test cases contain explicit mapping to user story SCM-012 and to a single acceptance criterion in both test plan and execution log. | SCM-012 | AC1-AC5 | Low |
| TP_SCM13_001 to TP_SCM13_015 | Direct | All SCM-013 test cases contain explicit mapping to user story SCM-013 and to a single acceptance criterion in both test plan and execution log. | SCM-013 | AC1-AC5 | Low |
| TP_SCM14_001 to TP_SCM14_015 | Direct | All SCM-014 test cases contain explicit mapping to user story SCM-014 and to a single acceptance criterion in both test plan and execution log. | SCM-014 | AC1-AC5 | Low |
| TP_SCM15_001 to TP_SCM15_015 | Direct | All SCM-015 test cases contain explicit mapping to user story SCM-015 and to a single acceptance criterion in both test plan and execution log. | SCM-015 | AC1-AC5 | Low |
| TP_SCM16_001 to TP_SCM16_015 | Direct | All SCM-016 test cases contain explicit mapping to user story SCM-016 and to a single acceptance criterion in both test plan and execution log. | SCM-016 | AC1-AC5 | Low |
| TP_SCM17_001 to TP_SCM17_015 | Direct | All SCM-017 test cases contain explicit mapping to user story SCM-017 and to a single acceptance criterion in both test plan and execution log. | SCM-017 | AC1-AC5 | Low |
| TP_SCM18_001 to TP_SCM18_015 | Direct | All SCM-018 test cases contain explicit mapping to user story SCM-018 and to a single acceptance criterion in both test plan and execution log. | SCM-018 | AC1-AC5 | Low |
| TP_SCM19_001 to TP_SCM19_015 | Direct | All SCM-019 test cases contain explicit mapping to user story SCM-019 and to a single acceptance criterion in both test plan and execution log. | SCM-019 | AC1-AC5 | Low |

## Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM10_001 to TP_SCM10_015 | Direct | All SCM-010 test cases contain explicit mapping to user story SCM-010 and to a single acceptance criterion in both test plan and execution log. | SCM-010 | AC1-AC5 | Low |
| TP_SCM11_001 to TP_SCM11_015 | Direct | All SCM-011 test cases contain explicit mapping to user story SCM-011 and to a single acceptance criterion in both test plan and execution log. | SCM-011 | AC1-AC5 | Low |
| TP_SCM12_001 to TP_SCM12_015 | Direct | All SCM-012 test cases contain explicit mapping to user story SCM-012 and to a single acceptance criterion in both test plan and execution log. | SCM-012 | AC1-AC5 | Low |
| TP_SCM13_001 to TP_SCM13_015 | Direct | All SCM-013 test cases contain explicit mapping to user story SCM-013 and to a single acceptance criterion in both test plan and execution log. | SCM-013 | AC1-AC5 | Low |
| TP_SCM14_001 to TP_SCM14_015 | Direct | All SCM-014 test cases contain explicit mapping to user story SCM-014 and to a single acceptance criterion in both test plan and execution log. | SCM-014 | AC1-AC5 | Low |
| TP_SCM15_001 to TP_SCM15_015 | Direct | All SCM-015 test cases contain explicit mapping to user story SCM-015 and to a single acceptance criterion in both test plan and execution log. | SCM-015 | AC1-AC5 | Low |
| TP_SCM16_001 to TP_SCM16_015 | Direct | All SCM-016 test cases contain explicit mapping to user story SCM-016 and to a single acceptance criterion in both test plan and execution log. | SCM-016 | AC1-AC5 | Low |
| TP_SCM17_001 to TP_SCM17_015 | Direct | All SCM-017 test cases contain explicit mapping to user story SCM-017 and to a single acceptance criterion in both test plan and execution log. | SCM-017 | AC1-AC5 | Low |
| TP_SCM18_001 to TP_SCM18_015 | Direct | All SCM-018 test cases contain explicit mapping to user story SCM-018 and to a single acceptance criterion in both test plan and execution log. | SCM-018 | AC1-AC5 | Low |
| TP_SCM19_001 to TP_SCM19_015 | Direct | All SCM-019 test cases contain explicit mapping to user story SCM-019 and to a single acceptance criterion in both test plan and execution log. | SCM-019 | AC1-AC5 | Low |

## Consistency Metrics Summary

| Metric | Count |
|---|---|
| Total test cases | 150.00 |
| Total test logs | 150.00 |
| Missing test cases | 0.00 |
| Missing test logs | 0.00 |
| Duplicate mappings identified | 0.00 |
| Ambiguous mappings identified | 0.00 |
| Overall consistency status | Consistent |

## Defect Details

| User Story ID | AC ID | Defect ID | Test Case ID | Defect Title / Description |
|---|---|---|---|---|
| SCM-010 | AC2 | DEF-SCM10-101 | TP_SCM10_005 | Reminder notification omits current plan price for annual-billed subscriptions |
| SCM-010 | AC5 | DEF-SCM10-102 | TP_SCM10_012 | Subscription remains active state after 3rd failed retry instead of moving to suspended |
| SCM-011 | AC5 | DEF-SCM11-101 | TP_SCM11_013 | Prorated refund calculation returns small negative value for last-day-of-cycle cancellations |
| SCM-011 | AC1 | DEF-SCM11-102 | TP_SCM11_014 | Duplicate cancellation request accepted when subscription already pending cancellation |
| SCM-012 | AC3 | DEF-SCM12-101 | TP_SCM12_014 | Feature access delayed by several minutes for upgrades processed at midnight billing boundary |
| SCM-012 | AC2 | DEF-SCM12-102 | TP_SCM12_015 | Prorated charge incorrectly applied at full price when upgrade occurs on last day of billing cycle |
| SCM-013 | AC2 | DEF-SCM13-101 | TP_SCM13_005 | Revoking license from team member with no assignment returns generic server error instead of handled message |
| SCM-013 | AC5 | DEF-SCM13-102 | TP_SCM13_012 | License pool count briefly shows incorrect total when revoke and reassign occur within same second |
| SCM-014 | AC4 | DEF-SCM14-101 | TP_SCM14_009 | Refund reason field truncated to 50 characters in audit log for long free-text reasons |
| SCM-014 | AC2 | DEF-SCM14-102 | TP_SCM14_013 | Refund request above threshold processed automatically before finance manager approval recorded |
| SCM-015 | AC1 | DEF-SCM15-101 | TP_SCM15_013 | Conversion attempted using expired payment method instead of failing over to downgrade path |
| SCM-015 | AC3 | DEF-SCM15-102 | TP_SCM15_014 | Downgrade notification not sent when conversion fails due to invalid (vs missing) payment method |
| SCM-016 | AC2 | DEF-SCM16-101 | TP_SCM16_013 | Prorated charge for add-on added on last day of billing cycle rounds up to full month charge |
| SCM-016 | AC4 | DEF-SCM16-102 | TP_SCM16_015 | Audit log merges two rapid add-on actions into a single entry, losing the first action |
| SCM-017 | AC2 | DEF-SCM17-101 | TP_SCM17_012 | International card format with alphanumeric routing details rejected as invalid |
| SCM-017 | AC4 | DEF-SCM17-102 | TP_SCM17_015 | No audit log entry created when payment method update fails midway through processing |
| SCM-018 | AC1 | DEF-SCM18-101 | TP_SCM18_011 | Consecutive failure counter does not reset after an intervening successful payment |
| SCM-018 | AC4 | DEF-SCM18-102 | TP_SCM18_014 | Suspension audit log omits failed attempts that occurred in a prior billing cycle |
| SCM-019 | AC1 | DEF-SCM19-101 | TP_SCM19_012 | Only one of several simultaneous tier price changes is detected and flagged for notification |
| SCM-019 | AC5 | DEF-SCM19-102 | TP_SCM19_015 | Downgrade request submitted on effective date boundary is charged a penalty fee in error |

## Conclusion

The unit test set is structurally consistent and complete at the document level, but overall quality readiness is constrained by 16 partially covered acceptance criteria and 20 logged defects, including failures in core billing, audit, retry, timing-boundary, and notification behaviors. Remediation should prioritize closure of failed edge and control-path tests, then add explicit test coverage for omitted AC obligations such as timing thresholds, audit attributes, portal detail fields, approval controls, SLA validation, and required notifications before sign-off.