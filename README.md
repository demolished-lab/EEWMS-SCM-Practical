# EEWMS Software Configuration Management Practical

This repository demonstrates a Git-based Software Configuration Management (SCM) workflow for an illustrative Employee Engagement and Wellness Management System (EEWMS) Software Requirements Specification (SRS).

## What the history demonstrates

- Baseline SRS commit (`v1.0`) and annotated baseline tag
- Change Request 1 on `feature/engagement-enhancements`, then merge to `main`
- Change Request 2 on `feature/privacy-security-enhancements`, then merge to `main`
- Final release tag `v2.0`
- History inspection and source-document comparison using Git

## Source of requirements

The requirements in `docs/SRS.md` are illustrative example content prepared for this SCM practical. They are not extracted from, nor evidence of approval for, a separately supplied or existing EEWMS SRS. The editable Markdown source is version-controlled because Git can show meaningful textual diffs; PDFs can be generated from approved source versions when needed.

## Versioning convention

- SRS revision `1.0`: initial illustrative baseline
- SRS revision `1.1`: engagement and HR analytics change request
- SRS revision `1.2`: privacy and security change request
- Git tag `v2.0`: release marker for the combined updated SRS
