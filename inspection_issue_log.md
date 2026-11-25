# Inspection Issue Log

**Project:** SNU Research Grants Management System (Group 11 SRS draft)
**Meeting Date:** 2026-11-23
**Recorder:** Yafet Teclu

- **Type:**
	- For individual requirements: **Incomplete** (missing parts), **Invalid** (does not follow from stakeholder needs), **Infeasible**, **Ambiguous**, **Unverifiable**, **Untraceable**.
	- For sets (e.g. the entire feature): **Incomplete**, **Inconsistent**, **Untraceable**
- **Severity:** **Major**, **Minor**
- **Location:** Section and file (the draft is Markdown, so no page numbers).

## Issues

| #   | Type | Severity | Location | Description |
| --- | ---- | -------- | -------- | ----------- |
| 1 | Ambiguous | Minor | 1.2 | 1.2 says requirements use "shall" or "must", but the draft uses "possibly" (2.2.4) and "should" (4.3.3), so it is unclear what is mandatory. |
| 2 | Untraceable | Minor | 2.2.1 | Applicant preparation and submission cites use case 3.2.1, which is the Chair signature use case. Submission is 3.1.2. |
| 3 | Untraceable | Minor | 2.2.1 | The applicant's Chair-signature function cites 3.3.1, which is intake and release. The signature use case is 3.2.1. |
| 4 | Untraceable | Major | 2.2.1, 2.2.3 | Application correction cites 3.4.1, which does not exist. The relevant use case is 3.2.2. |
| 5 | Untraceable | Minor | 2.2.1 | Application status tracking cites 3.6.1. The documented tracking use case is 3.3.2. |
| 6 | Untraceable | Major | 2.2.3, 2.2.4 | Research Officer intake and release (and reviewer access to released submissions) cites 3.5.1. The actual use case is 3.3.1. |
| 7 | Incomplete | Major | 2.2.3, 2.4.3 | The Research Officer must assign and maintain roles, but none of the six use cases covers role creation, change, removal or authorization. |
| 8 | Incomplete | Major | 2.2.4 to 2.2.6 | Confidential reviewer grading, funding decision recording and signed letter generation and release are promised, but no use case defines them. |
| 9 | Incomplete | Minor | 2.2.6 | The Dean's "monitor process efficiency and system usage" has no corresponding function or output. |
| 10 | Ambiguous | Minor | 2.4.2 | Traceability uses "should reference" for code, tests and commits, so it is unclear whether it is mandatory. |
| 11 | Inconsistent | Minor | 2.4.2 | The text says every requirement has a unique ID, but the mandatory constraints in Section 2 are prose without IDs. |
| 12 | Ambiguous | Minor | 2.5 | The system must work by the "next October adjudication cycle", but no year or readiness acceptance condition is given. |
| 13 | Incomplete | Minor | 3.1.1 | No authentication precondition, both Alternative Flow 1 and Exception 1 are "N/A", and nothing covers a cycle whose deadline has not been published. |
| 14 | Inconsistent | Major | 3.1.2 | The precondition says HR and SIS are checked at sign-in. 5.2 and 2.5 say eligibility is checked per protected action, and SIS is used only for student CoR reviewers. |
| 15 | Incomplete | Major | 3.2.1, 3.2.2 | Neither says whether editing an application after the Chair signs invalidates the signature or requires re-approval. |
| 16 | Ambiguous | Major | 3.2.2 | Exception 1 leaves an open question in the spec (whether the Research Officer refers the applicant to the Department Chair or the CoR Chair). The quality requirement says "flag" a request above the cap without saying whether it blocks or only warns. |
| 17 | Inconsistent | Major | 3.3.1 | 3.3.1 traces to BR-17, which says "all nine CoR members", but BR-8 and 2.2.4 define 11 reviewers (nine faculty plus two students). |
| 18 | Incomplete, Ambiguous | Minor | 3.3.2 | No error handling for opening a purged application or another applicant's record, the notification channel (email, in-app or both) is unspecified, and the decision letter fields beyond the award amount are unspecified. Consider splitting into two rows. |
| 19 | Inconsistent | Major | 4.3.1 | The first rule says applications are accepted only while the submission window is open, but the next rule allows submissions after the deadline until CoR release. |
| 20 | Untraceable | Minor | 4.3.1 | Late-application and Chair-signature constraints cite 3.2.1, 3.5.1 and 3.3.1, which are wrong or nonexistent use cases. |
| 21 | Inconsistent | Minor | 4.3.1 | The data-source table calls CoR the "Committee of Review"; the SRS elsewhere defines it as the "Committee on Research". (Recorded without a type; the preparation notes call it Inconsistent, Minor.) |
| 22 | Untraceable | Minor | 4.3.2 | Validation and release controls cite nonexistent use cases 3.4.1 and 3.5.1 instead of 3.2.2 and 3.3.1. |
| 23 | Inconsistent | Major | 4.3.3 | Retention starts at the "end of awards season", but no event or date defines it, so the three-year deletion deadline can't be determined. (The preparation notes call this Ambiguous, Major; confirm the type.) |
| 24 | Inconsistent | Major | 4.3.3 | Records must be purged from all copies after three years, but "respective schedules" for backups, exports and logs could let copies outlast that maximum. |
| 25 | Unverifiable | Minor | 4.3.3 | "Should" is used for scheduled deletion, and the purge method, schedule and evidence criteria are unconfirmed, so compliance can't be verified. |
| 26 | Incomplete | Major | 5.2.3 | `verifyFacultyStatus(email)` returns no academic rank or junior faculty flag, so the HR interface cannot verify BR-4 (only junior faculty may apply to JF) unless the system trusts self-entered rank. |
| 27 | Incomplete | Minor | 5.2.5 | No exact error message text, and no handling of a prolonged HR outage right before a deadline. |
| 28 | Unverifiable | Major | 6.1 | QA-01 names critical periods but gives no approved uptime percentage, measurement window or acceptable downtime. The 99.9% figure is only an unapproved assumption in 2.5. |
| 29 | Untraceable | Minor | 6.1 | QA-01 and QA-02 have no acceptance-test references in their related-tests metadata. |
| 30 | Untraceable | Minor | 6.2 | QA-02 leaves author, accountable, consult and inform blank and has no related business rule or evidence links. |
| 31 | Incomplete | Minor | 6.2 | The restart tests cover evaluation and funding decision records, but those recording use cases are not in the draft, so they can't be cross-checked. |
| 32 | Incomplete | Major | 4.1 | The ER diagram file is empty (0 bytes), so entities, relationships and cardinalities can't be examined. |
| 33 | Incomplete | Major | 4.2 | The data dictionary file is empty (0 bytes), so attributes, formats and valid values are undefined. |
| 34 | Incomplete | Minor | 6.3 | Robustness has no requirements and no explicit N/A justification. |
| 35 | Incomplete | Minor | 6.4 | Integrity is empty and doesn't reference the controls in 4.3.2. |
| 36 | Incomplete | Major | 6.5 | The Security section is empty, although confidentiality, authorization and encryption obligations are stated elsewhere. |
| 37 | Incomplete | Major | 6.6 | No measurable performance requirements for deadline-sensitive functions such as submission, approval and status tracking. |
| 38 | Incomplete | Minor | 6.7 | Interoperability is empty, with no N/A and no reference to the Keycloak, HR and SIS interfaces. |
| 39 | Inconsistent | Minor | 6.7 | The subsection is numbered 6.7 in Main.md, but its linked file is numbered 6.4. |
| 40 | Untraceable | Minor | 6.1 to 6.7 | Most Section 6 links omit the `.md` extension and point to paths that don't exist in the submitted archive. |
| 41 | Inconsistent | Major | BR-8, BR-17 | BR-8 defines nine faculty plus two student reviewers (11), but BR-17 says "all nine CoR members", leaving out the students. (Same root as row 17) |
| 42 | Incomplete | Major | BR-4, BR-10, BR-12 | BR-12 defines eligibility only for reviewers, not applicants. BR-4 never defines "junior faculty". BR-10 omits the grading scale, tie-breaking and conflict-of-interest rules. |
| 43 | Infeasible | Major | BR-13 | Requires purging backups and exports after three years, but 2.3 and 2.4.3 say IT controls backups separately and the system can't delete external exports. It also doesn't state when the clock starts. |
| 44 | Inconsistent | Minor | BR-10, BR-19 | BR-19 duplicates the second bullet of BR-10 (a target number set upfront and the top N funded). |
| 45 | Incomplete | Major | Appendix, Domain Evidence | The original interview transcripts are not in the submitted zip, so no citation can be checked and requirements can't be traced to stakeholders. |

**Totals:** 45 rows. Major: 21 (rows 4, 6, 7, 8, 14, 15, 16, 17, 19, 23, 24, 26, 28, 32, 33, 36, 37, 41, 42, 43, 45). Minor: 24.

---
*Copyright © 2001 by Karl E. Wiegers. Permission is granted to use, modify, and distribute this document.*
