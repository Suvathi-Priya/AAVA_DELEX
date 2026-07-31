# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report covers 10 user stories (SCM-001, SCM-010, SCM-011, SCM-012, SCM-013, SCM-014, SCM-015, SCM-016, SCM-017, SCM-018, SCM-019 files listed contain 10 complete user story sets excluding no gaps in listed set count logic for reportable stories from SCM-001 and SCM-010 through SCM-019), 50 acceptance criteria, 150 planned unit test cases, and 150 corresponding unit test log entries derived directly from the uploaded source documents. Document integrity is acceptable for reporting purposes: each user story contains an identifiable ID, title, and acceptance criteria; each test plan contains test case IDs and mapped acceptance criteria IDs; each test log contains execution status per test case; no standalone defect log documents were provided, so defect details were derived from the defect fields embedded in the uploaded test log documents.

Coverage across the uploaded scope is complete at AC presence level, with all 50 acceptance criteria having at least one mapped test case; however, quality gaps remain where requirements are only partially validated against their stated business obligations, especially where AC wording implies multiple obligations but the plan validates only a subset. Consistency review shows the testcase-to-AC/user-story mapping is structurally direct and consistent across all uploaded plans and logs, with no missing test cases, no missing test logs, and no duplicate or ambiguous mappings identifiable from the source content.

## Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-001 | AC5 | Fraud review obligation not explicitly validated; tests cover manager approval threshold behavior but do not evidence separate fraud review validation. | Partially Covered |
| SCM-010 | AC2 | 7-day advance timing obligation not explicitly validated; tests confirm reminder content and duplicate prevention but do not validate minimum advance-notice timing. | Partially Covered |
| SCM-010 | AC4 | Payment method used not explicitly validated in audit log coverage; tests validate subscription ID and renewal date only. | Partially Covered |
| SCM-011 | AC1 | Customer-initiated cancellation path not explicitly validated; coverage demonstrates administrator initiation only. | Partially Covered |
| SCM-011 | AC3 | Effective end date visibility not explicitly validated; tests cover cancellation status visibility only. | Partially Covered |
| SCM-011 | AC5 | Finance team review before refund issuance not explicitly validated; tests cover prorated refund calculation only. | Partially Covered |
| SCM-012 | AC4 | Prorated amount and effective date not explicitly validated in audit log coverage; tests validate previous/new plan and timestamp only. | Partially Covered |
| SCM-013 | AC3 | License expiration visibility not explicitly validated; tests cover assignment status only. | Partially Covered |
| SCM-014 | AC4 | Approver field not explicitly validated in audit log coverage for approval-required refunds. | Partially Covered |
| SCM-015 | AC2 | Specific reminder lead time obligation not explicitly validated; tests confirm reminder dispatch and content only. | Partially Covered |
| SCM-016 | AC3 | Total subscription cost visibility not explicitly validated; tests cover active add-ons and individual charges only. | Partially Covered |
| SCM-016 | AC5 | Regional regulation exception handling for retroactive refund not explicitly validated. | Partially Covered |
| SCM-017 | AC4 | Old payment method reference not explicitly validated; failed-update audit behavior also defective. | Partially Covered |
| SCM-017 | AC5 | Immediate retry using new payment method not explicitly validated; test confirms pending retry state only, not triggered retry execution. | Partially Covered |
| SCM-018 | AC3 | Outstanding balance visibility not explicitly validated; tests cover suspension status only. | Partially Covered |
| SCM-018 | AC5 | Defined SLA restoration timing not explicitly validated; tests cover reinstatement and payment precondition only. | Partially Covered |
| SCM-019 | AC2 | 30-day advance notification timing not explicitly validated; tests cover notification content and duplicate prevention only. | Partially Covered |
| SCM-019 | AC4 | Old price and new price audit capture not explicitly validated; tests cover subscription ID, notification date, and timestamp only. | Partially Covered |

## Consistency Analysis

| Testcase ID / Scope | Consistency Type | Description | Mapped User Story ID | Mapped AC ID | Impact Level |
|---|---|---|---|---|---|
| All uploaded test cases | Direct | Each testcase in every uploaded test plan includes an explicit acceptance criteria ID and mapped story ID, and each corresponding test log preserves the same mapping. | ALL | ALL | Low |
| All uploaded test logs | Direct | Every planned testcase has a corresponding execution log entry; no missing log evidence identified. | ALL | ALL | Low |
| All uploaded defects | Inferable-Direct | No separate defect log was provided; defect linkage was derived directly from defect ID/description fields embedded in test log rows. | ALL | Associated logged ACs | Medium |

## Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| All uploaded test cases | Direct | Each testcase in every uploaded test plan includes an explicit acceptance criteria ID and mapped story ID, and each corresponding test log preserves the same mapping. | ALL | ALL | Low |
| All uploaded test logs | Direct | Every planned testcase has a corresponding execution log entry; no missing log evidence identified. | ALL | ALL | Low |
| All uploaded defects | Inferable-Direct | No separate defect log was provided; defect linkage was derived directly from defect ID/description fields embedded in test log rows. | ALL | Associated logged ACs | Medium |

## Consistency Metrics Summary

| Metric | Count |
|---|---|
| Total Test Cases | 150 |
| Total Test Logs | 150 |
| Missing Test Cases | 0 |
| Missing Test Logs | 0 |
| Consistency Status | Consistent |

## Defect Details

| User Story ID | AC ID | Defect ID | Test Case ID | Defect Title / Description |
|---|---|---|---|---|
| SCM-001 | AC2 | DEF-SCM1-001 | UT_SCM1_005 | Notification template rendering issue |
| SCM-001 | AC5 | DEF-SCM1-002 | UT_SCM1_009 | Refund workflow synchronization error |
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

Unit test documentation and execution evidence are structurally complete and mapping-consistent, but several acceptance criteria are only partially covered against their full business obligations and 22 defects were identified across critical processing, boundary, notification, retry, and audit behaviors. Remediation should prioritize closure of failed scenarios and addition of missing obligation-level tests for timing, review/approval sub-flows, audit field completeness, portal detail visibility, and SLA/exception handling before quality sign-off.