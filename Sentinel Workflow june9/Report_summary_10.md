# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 5 user stories. The scope is restricted to test plans and execution records mapped to these user stories. Analysis excludes non-unit test activities and unrelated defect categories. The total number of user stories included in the analysis is 5, which form the baseline for evaluation. The scope is limited to unit test coverage and execution records mapped to these user stories.

## Test Coverage Summary

| User Story ID | Title | Total Acceptance Criterias | Fully Covered Acceptance Criterias | Partially Covered Acceptance Criterias | Not Covered Acceptance Criterias | Coverage Score Percentage | Total Test Cases in Test Plan | Total Test Cases in Test Logs | Total Passed | Total Failed | Total Defects |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| SCM-002 | Subscription Pause Management Service | 5 | 1 | 4 | 0 | 20.00 | 15 | 15 | 13 | 2 | 2 |
| SCM-003 | Subscription Upgrade Request Processing | 5 | 2 | 3 | 0 | 40.00 | 15 | 15 | 14 | 1 | 1 |
| SCM-004 | Subscription Cancellation Workflow | 5 | 3 | 2 | 0 | 60.00 | 15 | 15 | 14 | 1 | 1 |
| SCM-005 | Subscription Renewal Reminder Service | 5 | 4 | 1 | 0 | 80.00 | 15 | 15 | 14 | 1 | 1 |
| SCM-006 | Subscription Downgrade Request Management | 5 | 3 | 2 | 0 | 60.00 | 15 | 13 | 12 | 1 | 1 |

| Metric | Value |
|---|---|
| Total User Stories | 5 |
| Total Fully Covered User Stories | 0 |
| Total Partially Covered User Stories | 5 |
| Total Not Covered User Stories | 0 |
| Total Acceptance Criterias in All User Stories | 25 |
| Fully Covered Acceptance Criterias in All User Stories | 13 |
| Partially Covered Acceptance Criterias in All User Stories | 12 |
| Not Covered Acceptance Criterias in All User Stories | 0 |
| Overall Coverage Score Percentage | 52.00 |
| Overall Coverage Score Formula | (Fully Covered Acceptance Criteria in All User Stories / Total Acceptance Criteria in All User Stories) × 100 |
| Overall Coverage Score Calculation | (13 / 25) × 100 = 52.00 |
| Total Test Cases in All Test Plan | 75 |
| Total Test Cases in All Test Logs | 73 |
| Total Passed in All Test Logs | 67 |
| Total Failed in All Test Logs | 6 |
| Total Defects in All Test Logs | 6 |
| Overall Defect Rate Percentage | 8.00 |
| Overall Defect Rate Formula | (Total Defects / Total Test Cases) × 100 |
| Overall Defect Rate Calculation | (6 / 75) × 100 = 8.00 |

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-002 | AC2 | No testcase explicitly validates that resume date is included in pause confirmation notification. | Partially Covered |
| SCM-002 | AC3 | No testcase explicitly validates that scheduled resume date is viewable in the customer portal. | Partially Covered |
| SCM-002 | AC4 | No testcase explicitly validates that pause start date is captured in pause audit logs. | Partially Covered |
| SCM-002 | AC4 | No testcase explicitly validates that timestamp is captured in pause audit logs. | Partially Covered |
| SCM-002 | AC5 | No testcase explicitly validates that manager approval is required before the pause is activated. | Partially Covered |
| SCM-003 | AC2 | No testcase explicitly validates that revised billing amount is included in upgrade confirmation notification. | Partially Covered |
| SCM-003 | AC4 | No testcase explicitly validates that subscription ID is captured in upgrade audit logs. | Partially Covered |
| SCM-003 | AC4 | No testcase explicitly validates that upgrade date is captured in upgrade audit logs. | Partially Covered |
| SCM-003 | AC5 | No testcase explicitly validates that manager approval is required before the upgrade is activated. | Partially Covered |
| SCM-004 | AC2 | No testcase explicitly validates that applicable refund details are included in cancellation confirmation notification. | Partially Covered |
| SCM-004 | AC4 | No testcase explicitly validates that effective date is captured in cancellation audit logs. | Partially Covered |
| SCM-006 | AC2 | No testcase explicitly validates that adjusted billing amount is included in downgrade confirmation notification. | Partially Covered |

## Test Execution Summary

| Test Case ID | Status | Actual Result |
|---|---|---|
| TP_SCM_001 | Pass | Pause request submitted successfully |
| TP_SCM_002 | Pass | Pause start date captured successfully |
| TP_SCM_003 | Pass | Pause reason captured successfully |
| TP_SCM_004 | Pass | Notification sent successfully |
| TP_SCM_005 | Pass | Pause start date displayed in notification |
| TP_SCM_006 | Pass | Notification delivery recorded |
| TP_SCM_007 | Pass | Pause status displayed |
| TP_SCM_008 | Pass | Pause history displayed |
| TP_SCM_009 | Pass | Portal page accessible |
| TP_SCM_010 | Pass | Customer ID logged |
| TP_SCM_011 | Pass | Subscription ID logged |
| TP_SCM_012 | Fail | Pause reason missing in some records |
| TP_SCM_013 | Pass | Long duration pause identified |
| TP_SCM_014 | Pass | Approval workflow triggered |
| TP_SCM_015 | Fail | Pause activated before approval validation |
| TP_SCM3_001 | Pass | Upgrade request submitted successfully |
| TP_SCM3_002 | Pass | Preferred upgrade date captured successfully |
| TP_SCM3_003 | Pass | Invalid plan selection rejected with error |
| TP_SCM3_004 | Pass | Notification triggered after approval |
| TP_SCM3_005 | Fail | Revised billing amount missing in notification |
| TP_SCM3_006 | Pass | Delivery status recorded in system |
| TP_SCM3_007 | Pass | Upgrade request status displayed in portal |
| TP_SCM3_008 | Pass | Upgrade history list displayed correctly |
| TP_SCM3_009 | Pass | Next billing cycle change reflected in portal |
| TP_SCM3_010 | Pass | Customer ID recorded in audit log |
| TP_SCM3_011 | Pass | Previous and new plan recorded in audit log |
| TP_SCM3_012 | Pass | Timestamp recorded in audit log |
| TP_SCM3_013 | Pass | High-cost upgrade flagged by system |
| TP_SCM3_014 | Fail | Approval workflow not triggered for borderline 50% cases |
| TP_SCM3_015 | Pass | Manager notification generated |
| TP_SCM4_001 | Pass | Cancellation request submitted successfully |
| TP_SCM4_002 | Pass | Cancellation date saved successfully |
| TP_SCM4_003 | Pass | Empty reason rejected with validation error |
| TP_SCM4_004 | Pass | Cancellation confirmation notification sent |
| TP_SCM4_005 | Fail | Refund details missing from cancellation notification |
| TP_SCM4_006 | Pass | Delivery log entry created successfully |
| TP_SCM4_007 | Pass | Cancellation status displayed in portal |
| TP_SCM4_008 | Pass | Refund status displayed in portal |
| TP_SCM4_009 | Pass | Service end date displayed in portal |
| TP_SCM4_010 | Pass | Customer ID and subscription ID recorded |
| TP_SCM4_011 | Pass | Cancellation reason logged in audit |
| TP_SCM4_012 | Pass | Refund amount and timestamp recorded |
| TP_SCM4_013 | Pass | High balance cancellation flagged correctly |
| TP_SCM4_014 | Fail | Finance approval workflow not triggered consistently |
| TP_SCM4_015 | Pass | Cancellation held in pending state correctly |
| TP_SCM5_001 | Pass | 30-day reminder triggered on schedule |
| TP_SCM5_002 | Pass | 15-day reminder triggered on schedule |
| TP_SCM5_003 | Pass | 7-day reminder triggered on schedule |
| TP_SCM5_004 | Pass | Subscription name and expiry date present in reminder |
| TP_SCM5_005 | Fail | Renewal amount missing in 30-day reminder notification |
| TP_SCM5_006 | Pass | Renewal link included and functional |
| TP_SCM5_007 | Pass | Renewal schedule displayed in portal |
| TP_SCM5_008 | Pass | Reminder history list displayed |
| TP_SCM5_009 | Pass | Renewal preferences saved and applied |
| TP_SCM5_010 | Pass | Customer ID and subscription ID logged |
| TP_SCM5_011 | Pass | Reminder date and channel recorded |
| TP_SCM5_012 | Pass | Delivery status recorded in log |
| TP_SCM5_013 | Pass | High-value subscription identified correctly |
| TP_SCM5_014 | Pass | Customer notification sent for high-value subscriptions |
| TP_SCM5_015 | Fail | Account manager not notified for all high-value subscriptions |
| TP_SCM6_001 | Pass | Downgrade request submitted successfully |
| TP_SCM6_002 | Pass | Effective date saved successfully |
| TP_SCM6_003 | Pass | Upgrade plan rejected in downgrade flow |
| TP_SCM6_004 | Pass | Downgrade confirmation notification sent |
| TP_SCM6_005 | Fail | Adjusted billing amount absent in downgrade notification |
| TP_SCM6_006 | Pass | Delivery log entry created |
| TP_SCM6_007 | Pass | Downgrade status displayed in portal |
| TP_SCM6_008 | Pass | Plan comparison displayed correctly |
| TP_SCM6_009 | Pass | Credit adjustment amount displayed |
| TP_SCM6_010 | Pass | Customer ID and subscription ID recorded |
| TP_SCM6_011 | Pass | Previous and downgraded plan recorded |
| TP_SCM6_012 | Pass | Credit issued and timestamp recorded |
| TP_SCM6_013 | Pass | Enterprise downgrade flagged correctly |

## Consistency Analysis

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM6_014 | missing_testlog | Execution log is missing for testcase ID: TP_SCM6_014 | SCM-006 | AC5 | Medium |
| TP_SCM6_015 | missing_testlog | Execution log is missing for testcase ID: TP_SCM6_015 | SCM-006 | AC5 | Medium |

| Metric | Count |
|---|---|
| Total Test Cases | 75 |
| Total Test Logs | 73 |
| Missing Test Cases | 0 |
| Missing Test Logs | 2 |
| Consistency Status | Mismatch Detected |

## Defect Details

| Defect ID | Test Case ID | User Story ID | Defect Title | Defect Description |
|---|---|---|---|---|
| DEF-SCM-101 | TP_SCM_012 | SCM-002 | NULL | Pause reason not captured consistently |
| DEF-SCM-102 | TP_SCM_015 | SCM-002 | NULL | Activation allowed without completed approval |
| DEF-SCM3-101 | TP_SCM3_005 | SCM-003 | NULL | Revised billing amount not included in upgrade confirmation notification |
| DEF-SCM3-102 | TP_SCM3_014 | SCM-003 | NULL | Manager approval workflow not initiated when price increase equals exactly 50% |
| DEF-SCM4-101 | TP_SCM4_005 | SCM-004 | NULL | Applicable refund details not included in cancellation confirmation notification |
| DEF-SCM4-102 | TP_SCM4_014 | SCM-004 | NULL | Finance team approval workflow fails to initiate for accounts with mixed currency outstanding balances |
| DEF-SCM5-101 | TP_SCM5_005 | SCM-005 | NULL | Renewal amount not populated in 30-day reminder notification for monthly billing plans |
| DEF-SCM5-102 | TP_SCM5_015 | SCM-005 | NULL | Account manager reminder not sent when subscription value exceeds threshold but account manager assignment is pending |
| DEF-SCM6-101 | TP_SCM6_005 | SCM-006 | NULL | Adjusted billing amount not included in downgrade confirmation notification to customer |

## Conclusion

Remediation is required as multiple test cases have failed and defects exist across all user stories.
