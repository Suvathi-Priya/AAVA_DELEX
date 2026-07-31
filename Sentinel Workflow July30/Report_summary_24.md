# UNIT TEST QUALITY & COVERAGE REPORT

## Scope
This report covers 10 user stories (SCM-010 through SCM-019), 50 acceptance criteria, 150 planned unit test cases, and 150 corresponding unit test execution log entries. All listed user story, test plan, and test log documents were readable and structurally sufficient for analysis; no defect log files were separately provided, so defect details were derived from the defect references embedded in the execution logs.

Document completeness validation indicates each user story contains an identifiable ID, title, and acceptance criteria. Each test plan contains test case IDs and explicit acceptance-criteria mappings, and each test log contains execution status per test case. Derived consistency metrics show 0 missing test cases and 0 missing test logs, with full plan-to-log traceability across the submitted scope. Of the 50 acceptance criteria assessed, 50 are Fully Covered, 0 are Partially Covered, and 0 are Not Covered; however, multiple fully covered criteria contain failed executions and defect findings impacting quality readiness.

## Coverage Gap Details
| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-010 | AC1 | NULL | Fully Covered |
| SCM-010 | AC2 | NULL | Fully Covered |
| SCM-010 | AC3 | NULL | Fully Covered |
| SCM-010 | AC4 | Payment method used not explicitly validated; renewal amount not explicitly validated. | Fully Covered |
| SCM-010 | AC5 | NULL | Fully Covered |
| SCM-011 | AC1 | Customer-initiated cancellation path not explicitly validated. | Fully Covered |
| SCM-011 | AC2 | NULL | Fully Covered |
| SCM-011 | AC3 | Effective end date not explicitly validated. | Fully Covered |
| SCM-011 | AC4 | NULL | Fully Covered |
| SCM-011 | AC5 | Finance team review before refund issuance not explicitly validated. | Fully Covered |
| SCM-012 | AC1 | NULL | Fully Covered |
| SCM-012 | AC2 | NULL | Fully Covered |
| SCM-012 | AC3 | NULL | Fully Covered |
| SCM-012 | AC4 | Prorated amount not explicitly validated; effective date not explicitly validated. | Fully Covered |
| SCM-012 | AC5 | NULL | Fully Covered |
| SCM-013 | AC1 | Specified team member identity field not explicitly validated. | Fully Covered |
| SCM-013 | AC2 | NULL | Fully Covered |
| SCM-013 | AC3 | Expiration not explicitly validated. | Fully Covered |
| SCM-013 | AC4 | NULL | Fully Covered |
| SCM-013 | AC5 | Administrator notification of limit not explicitly validated. | Fully Covered |
| SCM-014 | AC1 | NULL | Fully Covered |
| SCM-014 | AC2 | NULL | Fully Covered |
| SCM-014 | AC3 | NULL | Fully Covered |
| SCM-014 | AC4 | Approver field not explicitly validated. | Fully Covered |
| SCM-014 | AC5 | NULL | Fully Covered |
| SCM-015 | AC1 | NULL | Fully Covered |
| SCM-015 | AC2 | Specific reminder lead time not explicitly validated. | Fully Covered |
| SCM-015 | AC3 | NULL | Fully Covered |
| SCM-015 | AC4 | NULL | Fully Covered |
| SCM-015 | AC5 | NULL | Fully Covered |
| SCM-016 | AC1 | Selection action not explicitly validated beyond browse/list behavior. | Fully Covered |
| SCM-016 | AC2 | NULL | Fully Covered |
| SCM-016 | AC3 | Total subscription cost not explicitly validated. | Fully Covered |
| SCM-016 | AC4 | NULL | Fully Covered |
| SCM-016 | AC5 | Regional-regulation exception path not explicitly validated. | Fully Covered |
| SCM-017 | AC1 | NULL | Fully Covered |
| SCM-017 | AC2 | NULL | Fully Covered |
| SCM-017 | AC3 | NULL | Fully Covered |
| SCM-017 | AC4 | Old payment method reference not explicitly validated. | Fully Covered |
| SCM-017 | AC5 | Immediate retry using new payment method not explicitly validated; only pending retry precondition is logged. | Fully Covered |
| SCM-018 | AC1 | NULL | Fully Covered |
| SCM-018 | AC2 | NULL | Fully Covered |
| SCM-018 | AC3 | Outstanding balance not explicitly validated. | Fully Covered |
| SCM-018 | AC4 | NULL | Fully Covered |
| SCM-018 | AC5 | Defined SLA restoration timing not explicitly validated; full access restoration not explicitly validated. | Fully Covered |
| SCM-019 | AC1 | NULL | Fully Covered |
| SCM-019 | AC2 | 30-day advance timing not explicitly validated. | Fully Covered |
| SCM-019 | AC3 | NULL | Fully Covered |
| SCM-019 | AC4 | Old price and new price not explicitly validated in audit log. | Fully Covered |
| SCM-019 | AC5 | NULL | Fully Covered |

## Consistency Analysis
| Test Case ID | Consistency Type | Description | Mapped User Story ID | Mapped AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM10_001 to TP_SCM19_015 | Direct | All test cases in submitted plans contain explicit mapping to a single user story and acceptance criterion, and each logged execution aligns to the same identifiers. | SCM-010 to SCM-019 | AC1 to AC5 | Low |
| SCM-010 AC4 related tests | Partial-by-content | Test plan maps tests to AC4, but only subscription ID and renewal date are explicitly validated; payment method used and renewal amount elements in the AC are not directly evidenced by test cases. | SCM-010 | AC4 | Medium |
| SCM-011 AC1 related tests | Partial-by-content | Test plan maps tests to AC1, but evidence covers administrator initiation only; customer initiation path is not explicitly represented. | SCM-011 | AC1 | Medium |
| SCM-011 AC3 related tests | Partial-by-content | Test cases map to AC3, but effective end date is not explicitly validated in available cases. | SCM-011 | AC3 | Medium |
| SCM-011 AC5 related tests | Partial-by-content | Prorated refund calculation is validated, but finance review prior to issuance is not directly evidenced. | SCM-011 | AC5 | Medium |
| SCM-012 AC4 related tests | Partial-by-content | AC4 mapping exists, but previous plan/new plan and timestamp only are explicitly validated; prorated amount and effective date fields are not directly evidenced. | SCM-012 | AC4 | Medium |
| SCM-013 AC3 related tests | Partial-by-content | AC3 mapping exists, but expiration visibility is not explicitly tested. | SCM-013 | AC3 | Medium |
| SCM-013 AC5 related tests | Partial-by-content | Blocking at license limit is tested, but administrator notification of limit is not explicitly validated. | SCM-013 | AC5 | Medium |
| SCM-014 AC4 related tests | Partial-by-content | AC4 mapping exists, but approver field coverage is not explicitly evidenced. | SCM-014 | AC4 | Medium |
| SCM-015 AC2 related tests | Partial-by-content | Reminder notification is validated, but the specified lead-time parameter is not explicitly covered. | SCM-015 | AC2 | Medium |
| SCM-016 AC3 related tests | Partial-by-content | Active add-ons and individual charges are tested, but total subscription cost display is not explicitly evidenced. | SCM-016 | AC3 | Medium |
| SCM-016 AC5 related tests | Partial-by-content | Default no-refund rule is tested, but regional-regulation exception behavior is not explicitly covered. | SCM-016 | AC5 | Medium |
| SCM-017 AC4 related tests | Partial-by-content | Audit log coverage exists, but old payment method reference is not directly validated. | SCM-017 | AC4 | Medium |
| SCM-017 AC5 related tests | Ambiguous functional sufficiency | Only the pending retry precondition is explicitly tested; the required immediate retry using the new payment method is not directly evidenced. | SCM-017 | AC5 | High |
| SCM-018 AC3 related tests | Partial-by-content | Suspension status is tested, but outstanding balance visibility is not explicitly evidenced. | SCM-018 | AC3 | Medium |
| SCM-018 AC5 related tests | Partial-by-content | Reinstatement/payment gating is tested, but restoration within defined SLA and full-access restoration are not directly evidenced. | SCM-018 | AC5 | High |
| SCM-019 AC2 related tests | Partial-by-content | Notification content is tested, but minimum 30-day advance timing is not explicitly evidenced. | SCM-019 | AC2 | High |
| SCM-019 AC4 related tests | Partial-by-content | Audit logging is mapped, but old and new price field capture is not directly evidenced by test cases. | SCM-019 | AC4 | Medium |

## Data Mapping Inconsistency Details
| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM10_001 to TP_SCM19_015 | Direct | All test cases in submitted plans contain explicit mapping to a single user story and acceptance criterion, and each logged execution aligns to the same identifiers. | SCM-010 to SCM-019 | AC1 to AC5 | Low |
| SCM-010 AC4 related tests | Partial-by-content | Test plan maps tests to AC4, but only subscription ID and renewal date are explicitly validated; payment method used and renewal amount elements in the AC are not directly evidenced by test cases. | SCM-010 | AC4 | Medium |
| SCM-011 AC1 related tests | Partial-by-content | Test plan maps tests to AC1, but evidence covers administrator initiation only; customer initiation path is not explicitly represented. | SCM-011 | AC1 | Medium |
| SCM-011 AC3 related tests | Partial-by-content | Test cases map to AC3, but effective end date is not explicitly validated in available cases. | SCM-011 | AC3 | Medium |
| SCM-011 AC5 related tests | Partial-by-content | Prorated refund calculation is validated, but finance review prior to issuance is not directly evidenced. | SCM-011 | AC5 | Medium |
| SCM-012 AC4 related tests | Partial-by-content | AC4 mapping exists, but previous plan/new plan and timestamp only are explicitly validated; prorated amount and effective date fields are not directly evidenced. | SCM-012 | AC4 | Medium |
| SCM-013 AC3 related tests | Partial-by-content | AC3 mapping exists, but expiration visibility is not explicitly tested. | SCM-013 | AC3 | Medium |
| SCM-013 AC5 related tests | Partial-by-content | Blocking at license limit is tested, but administrator notification of limit is not explicitly validated. | SCM-013 | AC5 | Medium |
| SCM-014 AC4 related tests | Partial-by-content | AC4 mapping exists, but approver field coverage is not explicitly evidenced. | SCM-014 | AC4 | Medium |
| SCM-015 AC2 related tests | Partial-by-content | Reminder notification is validated, but the specified lead-time parameter is not explicitly covered. | SCM-015 | AC2 | Medium |
| SCM-016 AC3 related tests | Partial-by-content | Active add-ons and individual charges are tested, but total subscription cost display is not explicitly evidenced. | SCM-016 | AC3 | Medium |
| SCM-016 AC5 related tests | Partial-by-content | Default no-refund rule is tested, but regional-regulation exception behavior is not explicitly covered. | SCM-016 | AC5 | Medium |
| SCM-017 AC4 related tests | Partial-by-content | Audit log coverage exists, but old payment method reference is not directly validated. | SCM-017 | AC4 | Medium |
| SCM-017 AC5 related tests | Ambiguous functional sufficiency | Only the pending retry precondition is explicitly tested; the required immediate retry using the new payment method is not directly evidenced. | SCM-017 | AC5 | High |
| SCM-018 AC3 related tests | Partial-by-content | Suspension status is tested, but outstanding balance visibility is not explicitly evidenced. | SCM-018 | AC3 | Medium |
| SCM-018 AC5 related tests | Partial-by-content | Reinstatement/payment gating is tested, but restoration within defined SLA and full-access restoration are not directly evidenced. | SCM-018 | AC5 | High |
| SCM-019 AC2 related tests | Partial-by-content | Notification content is tested, but minimum 30-day advance timing is not explicitly evidenced. | SCM-019 | AC2 | High |
| SCM-019 AC4 related tests | Partial-by-content | Audit logging is mapped, but old and new price field capture is not directly evidenced by test cases. | SCM-019 | AC4 | Medium |

## Consistency Metrics Summary
| Metric | Count |
|---|---|
| Total Test Cases | 150 |
| Total Test Logs | 150 |
| Missing Test Cases | 0 |
| Missing Test Logs | 0 |
| Consistency Status | Consistent with content-level coverage qualification gaps |
| Explicit Mapping Coverage | 150 of 150 test cases mapped to user stories and ACs (100.00%) |
| Test Log Traceability | 150 of 150 planned test cases have execution results (100.00%) |

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

## Conclusion
Traceability completeness is strong and all submitted acceptance criteria are mapped to executed tests, but the test evidence contains 20 logged defects and several content-level validation gaps where AC elements are not explicitly tested. Remediation is required to resolve failed test cases and add targeted test coverage for unvalidated AC clauses before the scope can be considered quality-complete.
