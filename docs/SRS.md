# Employee Engagement and Wellness Management System (EEWMS)

## Software Requirements Specification

**Document revision:** 1.1  
**Status:** Illustrative requirements updated for CR-01  
**Change control:** This sample specification is not an approved production document.

## 1. Purpose and scope

EEWMS is a proposed internal system for collecting employee engagement feedback and presenting summary information to authorized Human Resources (HR) personnel. This compact example specification demonstrates version control and change tracking.

## 2. Users

- **Employee:** completes available pulse surveys.
- **HR analyst:** reviews summarized engagement indicators.
- **System administrator:** maintains system configuration and user access.

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

## 4. Non-functional requirements

- **NFR-01:** The system shall require authenticated access for HR and administrator functions.
- **NFR-02:** The system shall retain survey and response records according to the organization's approved retention policy.
- **NFR-03:** The system shall record administrative configuration changes in an audit log.
- **NFR-04:** The system shall document the engagement scoring method and the limitations of automated sentiment classification.

## 5. Assumptions and open items

- The organization will define its approved retention period, minimum reporting threshold, scoring method, and access policy before production deployment.
- This practical uses illustrative requirements only; stakeholder review and approval are required before a real SRS can become a controlled baseline.

## 6. Revision record

| Revision | Change | SCM reference |
| --- | --- | --- |
| 1.0 | Initial illustrative baseline | Baseline commit and tag `v1.0` |
| 1.1 | Pulse survey, engagement scoring, sentiment analysis, and dashboard enhancements | Change Request CR-01 |
