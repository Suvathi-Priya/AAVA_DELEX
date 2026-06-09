# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 6 user stories. The scope is restricted to test plans and execution records mapped to these user stories. Analysis excludes non-unit test activities and unrelated defect categories. These user stories form the baseline for evaluation, with the scope limited to unit test coverage and execution records mapped to CLP-001, CNS-001, ORM-001, SCM002, SCM-003, and SCM-004.

## Test Coverage Summary

| User Story ID | Title | Total Acceptance Criterias | Fully Covered Acceptance Criterias | Partially Covered Acceptance Criterias | Not Covered Acceptance Criterias | Coverage Score Percentage | Total Test Cases in Test Plan | Total Test Cases in Test Logs | Total Passed | Total Failed | Total Defects |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| CLP-001 | Customer Loyalty Program | 5 | 5 | 0 | 0 | 100.00 | 13 | 13 | 11 | 2 | 2 |
| CNS-001 | Customer Notification Service | 5 | 5 | 0 | 0 | 100.00 | 15 | 13 | 10 | 3 | 3 |
| ORM-001 | Order Refund Management | 5 | 5 | 0 | 0 | 100.00 | 15 | 15 | 12 | 3 | 3 |
| SCM002 | Subscription Pause Management | 5 | 5 | 0 | 0 | 100.00 | 15 | 15 | 13 | 2 | 2 |
| SCM-003 | Subscription Upgrade Management | 5 | 5 | 0 | 0 | 100.00 | 15 | 15 | 13 | 2 | 2 |
| SCM-004 | Subscription Cancellation Management | 0 | 0 | 0 | 0 | 0.00 | 0 | 15 | 13 | 2 | 2 |

| Metric | Value |
|---|---|
| Total User Stories | 6 |
| Total Fully Covered User Stories | 5 |
| Total Partially Covered User Stories | 0 |
| Total Not Covered User Stories | 1 |
| Total Acceptance Criterias in All User Stories | 25 |
| Fully Covered Acceptance Criterias in All User Stories | 25 |
| Partially Covered Acceptance Criterias in All User Stories | 0 |
| Not Covered Acceptance Criterias in All User Stories | 0 |
| Overall Coverage Score Percentage | 100.00 |
| Overall Coverage Score Formula | (Fully Covered Acceptance Criteria in All User Stories / Total Acceptance Criteria in All User Stories) × 100 |
| Overall Coverage Score Calculation | (25 / 25) × 100 = 100.00 |
| Total Test Cases in All Test Plan | 73 |
| Total Test Cases in All Test Logs | 73 |
| Total Passed in All Test Logs | 64 |
| Total Failed in All Test Logs | 9 |
| Total Defects in All Test Logs | 11 |
| Overall Defect Rate Percentage | 15.07 |
| Overall Defect Rate Formula | (Total Defects / Total Test Cases) × 100 |
| Overall Defect Rate Calculation | (11 / 73) × 100 = 15.07 |

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| No coverage gaps identified from coverage_analysis data |  |  |  |

## Test Execution Summary

| Test Case ID | Status | Actual Result |
|---|---|---|
| UT_CLP_001 | Passed | Points awarded successfully |
| UT_CLP_002 | Passed | Correct points calculated |
| UT_CLP_003 | Failed | Points posting delayed |
| UT_CLP_004 | Passed | Reward redeemed successfully |
| UT_CLP_005 | Passed | Points deducted correctly |
| UT_CLP_006 | Passed | Reward issued successfully |
| UT_CLP_007 | Passed | Balance displayed correctly |
| UT_CLP_008 | Failed | Balance refresh issue observed |
| UT_CLP_009 | Passed | Balance updated after redemption |
| UT_CLP_010 | Passed | Customer ID logged |
| UT_CLP_011 | Passed | Points value logged |
| UT_CLP_012 | Passed | Timestamp logged |
| UT_CLP_013 | Passed | Manager approval validated |
| UT_CNS_001 | Pass | Email notification delivered |
| UT_CNS_002 | Pass | Email content generated |
| UT_CNS_003 | Pass | Delivery status recorded |
| UT_CNS_004 | Fail | SMS not delivered |
| UT_CNS_005 | Pass | SMS content generated |
| UT_CNS_006 | Fail | Delivery status unavailable |
| UT_CNS_007 | Pass | Enable preference saved |
| UT_CNS_008 | Pass | Disable preference saved |
| UT_CNS_009 | Fail | Push notification not dispatched |
| UT_CNS_010 | Pass | Customer ID logged |
| UT_CNS_011 | Pass | Notification type logged |
| UT_CNS_012 | Pass | Log record created |
| UT_CNS_013 | Pass | Retry initiated |
| UT_ORM_001 | Pass | Refund request created |
| UT_ORM_002 | Pass | Refund ID generated |
| UT_ORM_003 | Pass | Refund request stored |
| UT_ORM_004 | Pass | Notification sent |
| UT_ORM_005 | Fail | Notification content generation failed |
| UT_ORM_006 | Pass | Delivery status recorded |
| UT_ORM_007 | Pass | Refund status displayed |
| UT_ORM_008 | Pass | Latest status displayed |
| UT_ORM_009 | Fail | Status history unavailable |
| UT_ORM_010 | Pass | Customer ID logged |
| UT_ORM_011 | Pass | Refund amount logged |
| UT_ORM_012 | Pass | Audit log created |
| UT_ORM_013 | Pass | Manager approval required |
| UT_ORM_014 | Pass | Fraud review initiated |
| UT_ORM_015 | Fail | High-value refund processing blocked |
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

## Consistency Analysis

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| UT_CLP_014 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_CLP_014 | CLP-001 | AC5 | High |
| UT_CLP_015 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_CLP_015 | CLP-001 | AC5 | High |
| UT_CNS_014 | missing_testlog | Execution log is missing for testcase ID: UT_CNS_014 | CNS-001 | AC5 | Medium |
| UT_CNS_015 | missing_testlog | Execution log is missing for testcase ID: UT_CNS_015 | CNS-001 | AC5 | Medium |
| TP_SCM4_001 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM4_001 | SCM-004 | AC1 | High |
| TP_SCM4_002 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM4_002 | SCM-004 | AC1 | High |
| TP_SCM4_003 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM4_003 | SCM-004 | AC1 | High |
| TP_SCM4_004 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM4_004 | SCM-004 | AC2 | High |
| TP_SCM4_005 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM4_005 | SCM-004 | AC2 | High |
| TP_SCM4_006 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM4_006 | SCM-004 | AC2 | High |
| TP_SCM4_007 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM4_007 | SCM-004 | AC3 | High |
| TP_SCM4_008 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM4_008 | SCM-004 | AC3 | High |
| TP_SCM4_009 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM4_009 | SCM-004 | AC3 | High |
| TP_SCM4_010 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM4_010 | SCM-004 | AC4 | High |
| TP_SCM4_011 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM4_011 | SCM-004 | AC4 | High |
| TP_SCM4_012 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM4_012 | SCM-004 | AC4 | High |
| TP_SCM4_013 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM4_013 | SCM-004 | AC5 | High |
| TP_SCM4_014 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM4_014 | SCM-004 | AC5 | High |
| TP_SCM4_015 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM4_015 | SCM-004 | AC5 | High |

| Metric | Count |
|---|---|
| Total Test Cases | 73 |
| Total Test Logs | 88 |
| Missing Test Cases | 17 |
| Missing Test Logs | 2 |
| Consistency Status | Mismatch Detected |

## Defect Details

| Defect ID | Test Case ID | User Story ID | Defect Description |
|---|---|---|---|
| DEF-CLP-001 | UT_CLP_003 | CLP-001 | DEF-CLP-001 - Points posting service delay |
| DEF-CLP-002 | UT_CLP_008 | CLP-001 | DEF-CLP-002 - Balance refresh cache issue |
| DEF-CLP-003 | UT_CLP_015 | CLP-001 | DEF-CLP-003 - Redemption workflow synchronization issue |
| DEF-CNS-001 | UT_CNS_004 | CNS-001 | DEF-CNS-001 - SMS gateway timeout prevents delivery |
| DEF-CNS-002 | UT_CNS_006 | CNS-001 | DEF-CNS-002 - SMS tracking service failed to update status |
| DEF-CNS-003 | UT_CNS_009 | CNS-001 | DEF-CNS-003 - Push notification service unavailable |
| DEF-ORM-001 | UT_ORM_005 | ORM-001 | DEF-ORM-001 - Notification template rendering issue |
| DEF-ORM-002 | UT_ORM_009 | ORM-001 | DEF-ORM-002 - Status history service timeout |
| DEF-ORM-003 | UT_ORM_015 | ORM-001 | DEF-ORM-003 - Refund workflow synchronization error |
| DEF-SCM-101 | TP_SCM_012 | SCM002 | DEF-SCM-101 - Pause reason not captured consistently |
| DEF-SCM-102 | TP_SCM_015 | SCM002 | DEF-SCM-102 - Activation allowed without completed approval |
| DEF-SCM3-101 | TP_SCM3_005 | SCM-003 | DEF-SCM3-101 - Revised billing amount not included in upgrade confirmation notification |
| DEF-SCM3-102 | TP_SCM3_014 | SCM-003 | DEF-SCM3-102 - Manager approval workflow not initiated when price increase equals exactly 50% |
| DEF-SCM4-101 | TP_SCM4_005 | SCM-004 | DEF-SCM4-101 - Applicable refund details not included in cancellation confirmation notification |
| DEF-SCM4-102 | TP_SCM4_014 | SCM-004 | DEF-SCM4-102 - Finance team approval workflow fails to initiate for accounts with mixed currency outstanding balances |

## Conclusion

Remediation is required as test case failures and defects exist across multiple user stories, indicating outstanding execution issues that must be addressed before progression.
