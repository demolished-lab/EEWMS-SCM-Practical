# Employee Engagement and Wellness Management System (EEWMS)

## Software Requirements Specification

**Document revision:** 1.0  
**Status:** Illustrative baseline for SCM practical  
**Change control:** This sample baseline is not an approved production specification.

## 1. Purpose and scope

EEWMS is a proposed internal system for collecting employee engagement feedback and presenting summary information to authorized Human Resources (HR) personnel. This document is a compact example specification used to demonstrate Git version control and change tracking.

## 2. Users

- **Employee:** completes an available pulse survey.
- **HR analyst:** reviews summarized engagement indicators.
- **System administrator:** maintains system configuration and user access.

## 3. Functional requirements

### 3.1 Pulse surveys

- **FR-01:** The system shall allow an authorized HR user to create a pulse survey with a title, questions, opening date, and closing date.
- **FR-02:** The system shall allow an employee to view and submit a survey that is open to that employee.
- **FR-03:** The system shall prevent a second submission by the same employee for the same survey.

### 3.2 Engagement reporting

- **FR-04:** The system shall calculate a survey participation rate from submitted responses and eligible employees.
- **FR-05:** The system shall display aggregate participation and engagement summaries to authorized HR users.

## 4. Non-functional requirements

- **NFR-01:** The system shall require authenticated access for HR and administrator functions.
- **NFR-02:** The system shall retain survey and response records according to the organization's approved retention policy.
- **NFR-03:** The system shall record administrative configuration changes in an audit log.

## 5. Assumptions and open items

- The organization will define its approved retention period and access policy before production deployment.
- This practical uses example requirements only; a real project must obtain stakeholder review and approval before treating the SRS as a controlled baseline.
