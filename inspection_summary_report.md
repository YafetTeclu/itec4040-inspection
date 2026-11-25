# Inspection Summary Report


## Inspection Identification

- **Project:** SNU Research Grants Management System (Group 11 SRS draft for inspection)
- **Meeting Date:** November 23, 2026

## Work Product Description

- Draft Software Requirements Specification (SRS) for the SNU Research Grants Management System, written by Group 11 and received in anonymized form as a zip file of Markdown files.
- Contents: Main.md (the SRS skeleton with Sections 1 to 6 and appendices), Section 2 (Overall Description), Section 3 (six use cases, 3.1.1 to 3.3.2), 4.3 (Data Acquisition, Integrity, Retention and Disposal), 5.2 (Software Interfaces), 6.1 and 6.2 (Availability, Reliability), Appendix B (20 business rules) and Appendix C (glossary).
- Files linked from Main.md but empty or absent in the zip: 4.1 ER diagram, 4.2 data dictionary, 6.3 to 6.7, and the interview evidence files.
- Metadata: all files carry the status "in progress" and no version number. The draft is Markdown, so there are no page numbers.

## Inspectors

| #   | Role      | Inspector | Preparation Time (hours) |
| --- | --------- | --------- | ------------------------ |
| 1   | Author    | Group 11  | n/a |
| 2   | Moderator | Rasmandeep | 2 |
| 3   | Recorder  | Yafet  | 2 |
| 4   | Reader    | Michael | 2 |
| 5   | Reader    | Balraj | 2 |
| 6   | Inspector | Michael | (included above) |
| 7   | Inspector | Balraj | (included above) |

## Inspection Data

| Metric                   | Value              |
| ------------------------ | ------------------ |
| Planned for Inspection   | 12 files (Markdown files; no page numbers) |
| Actually Inspected       | 12 files (Markdown; no page numbers) |
| Meeting Time             | 1 hour (recorded 3:06 pm to 4:07 pm; the group joined the call at 2:00 pm) |
| Total Planning Effort    | 1.5 labor hours |
| Total Overview Effort    | 1 labor hour |
| Total Preparation Effort | 8 labor hours  |
| Actual Rework Effort     | n/a (the author group performs rework) |

## Inspection Process Description

- **Planning:** the group coordinated through WhatsApp and met on Zoom at 2:00 pm on November 23.
- **Roles:** Rasmandeep was Moderator. Yafet was Recorder. Michael and Balraj were Readers and also inspected. Group 11, the author, was not part of the meeting.
- **Before the meeting:**
  - Each inspector read the draft and prepared point-form defect notes using the course checklists and issue types.
  - The sections were split between the readers: one covered Sections 1, 3, 5 and the Business Rules, the other covered Sections 2, 4, 6 and the Business Rules.
  - The recorder prepared a draft list of issues for the log.
- **Meeting:**
  - The Moderator ran the meeting on Zoom. The readers went through the draft section by section (Main.md and Section 1, Section 2, Section 3, Section 4, Section 5, Section 6, Business Rules).
  - Each reader summarized the section, and any inspector raised issues for it. The group agreed on the type and severity, and the Recorder logged each issue in the issue log.
  - The goal was to record issues, not to design fixes.
  - The meeting was recorded: https://www.youtube.com/watch?v=XMtpId2h3nI
- **Coverage:** the inspection covered every file supplied in the zip. Nothing was excluded, apart from the files the draft lacked (4.1, 4.2, 6.3 to 6.7 content and the interview transcripts), which were recorded as defects.
- **After the meeting:** the Recorder merged the issue log, matched descriptions to the preparation notes, and prepared this report.

## Summary of Issues

- 45 issues were logged: 21 Major and 24 Minor (see the issue log).
- **Cross-references:** Sections 2.2 and 4.3 cite use case numbers (3.2.1, 3.3.1, 3.4.1, 3.5.1, 3.6.1) that do not match Section 3. The same error appears in at least eight places, so a reader following a link reaches the wrong use case or none.
- **Missing content:** the ER diagram (4.1), the data dictionary (4.2), and the Security, Performance, Robustness, Integrity and Interoperability sections (6.3 to 6.7) are empty. No use cases cover role administration, confidential grading, funding decisions or decision letters, although Section 2 depends on them. The interview transcripts are not in the zip, so no requirement can be traced to evidence.
- **Contradictions:**
  - 3.1.2 says HR and SIS are checked at sign-in; 5.2 and 2.5 say they are checked per action.
  - BR-17 says "nine" CoR members while BR-8 defines 11 reviewers.
  - 4.3.1 allows late submissions after saying applications are accepted only while the window is open.
- **Ambiguous or unverifiable wording:** "should" and "possibly" appear despite the "shall or must" convention. The retention clock start ("end of awards season") and the purge schedule are undefined. QA-01 has no measurable target. The "flag" wording for funding-cap violations does not say whether submission is blocked.
- **Workflow gaps:** it is not stated whether editing an application invalidates the Department Chair's signature. The HR interface cannot verify junior faculty status for JF applicants.

## Product Appraisal

**RECOMMENDATION**
- [ ] accepted as is
- [ ] conditionally accepted upon verification
- [x] reinspect following rework
- [ ] inspection not completed

**OTHER COMMENTS**

The draft is well organized, and the use cases are consistent with the business rules in most places. However, several Major issues need rework before the final SRS: the use case cross-references in Sections 2 and 4.3 do not match Section 3; Sections 4.1, 4.2 and 6.3 to 6.7 are empty; the interview evidence is missing, so requirements cannot be traced to stakeholders; the retention start and purge schedule are undefined; and 3.1.2, BR-17 and 4.3.1 contradict other sections. We recommend that the author fix these and that the draft be re-inspected.


----
*Copyright © 2001 by Karl E. Wiegers. Permission is granted to use, modify, and distribute this document.*
