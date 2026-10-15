# Employee Engagement and Wellness Management System (EEWMS)

## Software Requirements Specification

**Document revision:** 1.2  
**Status:** Illustrative requirements updated for CR-02  
**Change control:** This sample specification is not an approved production document.

## 1. Purpose and scope

EEWMS is a proposed internal system for collecting employee engagement feedback and presenting summary information to authorized Human Resources (HR) personnel. This compact example specification demonstrates version control and change tracking.

## 2. Users and roles

- **Employee:** completes available pulse surveys and may submit feedback or a grievance.
- **HR analyst:** reviews privacy-protected aggregate engagement indicators.
- **HR case handler:** accesses only grievance cases assigned to that handler.
- **System administrator:** maintains system configuration and user access, but does not receive routine access to survey response content.

## 3. Functional requirements

### 3.1 Pulse surveys

- **FR-01:** The system shall allow an authorized HR user to create a pulse survey with a title, questions, opening date, closing date, and target employee group.
- **FR-02:** The system shall allow an employee to view and submit a survey that is open to that employee.
- **FR-03:** The system shall prevent a second submission by the same employee for the same survey.
- **FR-04:** The system shall allow an authorized HR user to schedule recurring pulse surveys and reuse approved question templates.
- **FR-05:** The system shall show survey availability and completion status to the employee without exposing other employees' responses.

### 3.2 Engagement scoring and sentiment analysis

- **FR-06:** The system shall calculate an engagement score from configured survey questions using a documented scoring method.
- **FR-07:** The system shall display score trends across survey periods and permit comparison by approved organizational group when the group meets the minimum reporting threshold.
- **FR-08:** The system shall optionally classify free-text responses into broad sentiment categories and shall label such classifications as automated estimates, not definitive judgments.
- **FR-09:** The system shall allow an authorized HR analyst to inspect aggregate sentiment summaries without revealing employee identity in the analytics view.

### 3.3 HR analytics dashboard

- **FR-10:** The dashboard shall show response rate, aggregate engagement score, and available trend summaries for selected periods.
- **FR-11:** The dashboard shall support filters for survey, time period, and approved organizational group, subject to privacy thresholds.
- **FR-12:** The dashboard shall distinguish measured response data from automated sentiment estimates and shall display the data period represented.

### 3.4 Anonymous feedback and grievance reporting

- **FR-13:** The system shall allow an employee to submit anonymous feedback without associating the response with the employee's account in the HR analytics view.
- **FR-14:** The system shall provide a separate grievance-reporting workflow that issues a non-identifying reference code so a reporter can check case status without disclosing identity.
- **FR-15:** The system shall clearly explain any limits to anonymity, including information voluntarily entered into free-text fields and legally required disclosures.
- **FR-16:** The system shall restrict grievance details to authorized case handlers assigned to the case and shall keep grievance records separate from aggregate engagement analytics.

## 4. Non-functional requirements

- **NFR-01:** The system shall require authenticated access for HR, case-handler, and administrator functions and enforce role-based permissions.
- **NFR-02:** The system shall retain survey, feedback, and grievance records according to the organization's approved retention policy and support authorized deletion at the end of that period.
- **NFR-03:** The system shall record access to sensitive records and administrative configuration changes in an audit log protected from ordinary user modification.
- **NFR-04:** The system shall document the engagement scoring method and limitations of automated sentiment classification.
- **NFR-05:** The system shall suppress or combine analytics results for groups below the organization's minimum reporting threshold to reduce re-identification risk.
- **NFR-06:** The system shall protect data in transit and at rest using organization-approved security controls.
- **NFR-07:** The system shall restrict exports of raw response and grievance data to specifically authorized roles and record such exports in the audit log.

## 5. Assumptions and open items

- The organization will define its approved retention period, minimum reporting threshold, scoring method, identity separation approach, role matrix, encryption standard, and access policy before production deployment.
- Anonymity has operational and legal limits; the production system must disclose those limits and receive privacy/legal review.
- This practical uses illustrative requirements only; stakeholder review and approval are required before a real SRS can become a controlled baseline.

## 6. Revision record

| Revision | Change | SCM reference |
| --- | --- | --- |
| 1.0 | Initial illustrative baseline | Baseline commit and tag `v1.0` |
| 1.1 | Pulse survey, engagement scoring, sentiment analysis, and dashboard enhancements | Change Request CR-01; tag `v1.1` |
| 1.2 | Anonymous feedback, grievance workflow, privacy-aware analytics, and security controls | Change Request CR-02 |
