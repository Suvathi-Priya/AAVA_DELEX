# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 1 user story. The scope is restricted to test plans and execution records mapped to these user stories. Analysis excludes non-unit test activities and unrelated defect categories. The user stories form the baseline for evaluation, and the scope is limited to unit test coverage and execution records mapped to these user stories.

## Test Coverage Summary

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-007 | AC2 | No testcase explicitly validates that transfer details are included in the notification. | Partially Covered |
| SCM-007 | AC3 | No testcase explicitly validates that the outgoing owner can view billing change summary in the customer portal. | Partially Covered |
| SCM-007 | AC3 | No testcase explicitly validates that the incoming owner can view billing change summary in the customer portal. | Partially Covered |
| SCM-007 | AC5 | No testcase explicitly validates that transfers involving a change in billing entity require compliance team approval. | Not Covered |
| SCM-007 | AC5 | No testcase explicitly validates that transfers involving a change in tax jurisdiction require compliance team approval. | Not Covered |
| SCM-007 | AC5 | No testcase explicitly validates that compliance team approval is required before the transfer is completed. | Not Covered |

## Test Execution Summary

| Test Case ID | Status | Actual Result | Defects |
|---|---|---|---|
| TP_SCM7_001 | Pass | Transfer request created successfully | |
| TP_SCM7_002 | Pass | Transfer effective date saved | |
| TP_SCM7_003 | Pass | Invalid new owner rejected by system | |
| TP_SCM7_004 | Pass | Current owner notified of transfer | |
| TP_SCM7_005 | Fail | New owner notification not sent in all transfer scenarios | DEF-SCM7-101 |
| TP_SCM7_006 | Pass | Effective date and billing detail present in notification | |
| TP_SCM7_007 | Pass | Transfer status visible to outgoing owner | |
| TP_SCM7_008 | Pass | Transfer status visible to incoming owner | |
| TP_SCM7_009 | Pass | Ownership history displayed in portal | |
| TP_SCM7_010 | Pass | Current and new owner IDs recorded | |
| TP_SCM7_011 | Pass | Subscription ID and transfer date recorded | |
| TP_SCM7_012 | Pass | Authorization reference and timestamp recorded | |
| TP_SCM7_013 | Pass | Compliance-sensitive transfer flagged correctly | |
| TP_SCM7_014 | Fail | Compliance team approval workflow not triggered for tax jurisdiction changes | DEF-SCM7-102 |
| TP_SCM7_015 | Pass | Transfer correctly held in pending state | |

## Consistency Analysis

### Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM7_014 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_014 | SCM-007 | AC5 | High |
| TP_SCM7_015 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_015 | SCM-007 | AC5 | High |

### Consistency Metrics Summary

| Metric | Count |
|---|---|
| Total Test Cases | 13 |
| Total Test Logs | 15 |
| Missing Test Cases | 2 |
| Missing Test Logs | 0 |
| Consistency Status | Mismatch Detected |

## Defect Details

| Defect ID | Test Case ID | User Story ID | Defect Description |
|---|---|---|---|
| DEF-SCM7-101 | TP_SCM7_005 | SCM-007 | New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint |
| DEF-SCM7-102 | TP_SCM7_014 | SCM-007 | Compliance approval workflow not initiated for transfers involving tax jurisdiction change only without entity change |

## Conclusion

Remediation is required as defects exist and user story AC5 is Not Covered.
