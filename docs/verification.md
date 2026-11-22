# Verification record

Checked **2026-11-22**, Linux/WSL2, during initial authoring. Inputs below are deliberately synthetic. These are bounded package and source-loaded behavior checks, not a hiring study, security audit, or ATS certification.

## Package contract check

Ran a temporary, dependency-free Node.js check against both skill packages. It checked the frontmatter's simple `name`/`description` form, naming constraints, directory/name agreement, nonempty descriptions within the specification's length bound, entrypoints under 500 lines, balanced code fences, LF line endings, absence of package symlinks, and existence/confinement of local reference links.

Observed output:

```text
PASS resume-writing: metadata, name agreement, standalone references, Markdown structure
PASS academic-cv: metadata, name agreement, standalone references, Markdown structure
PASS 2 skill packages; 3 bundled reference links resolved
```

This was a custom structural check of the metadata syntax actually used, not a full YAML parser, the upstream `skills-ref` validator, or a host discovery test. The temporary check ran inline and left no script or dependency in the repository.

## Documentation link check

A separate inline Node.js check resolved local Markdown links and GitHub-style heading anchors in `README.md`, `AGENTS.md`, `SOURCES.md`, `examples/requests.md`, and this record.

```text
PASS 5 documentation files; 41 local links and 23 section anchors resolved
```

External source access and its limits are recorded in `SOURCES.md`; this link check did not retry external URLs or test rendered GitHub appearance.

## Source-loaded résumé scenarios

A consuming agent explicitly read:

- `skills/resume-writing/SKILL.md`
- `skills/resume-writing/references/writing-guide.md`
- `skills/resume-writing/references/ats-and-export.md`

The agent then produced actual draft/review responses using synthetic inputs. The parent inspected the returned outputs, not only the agent's pass labels. No original/baseline skill was run, so no comparative improvement is claimed.

| Scenario and input | Observed behavior | Result |
| --- | --- | --- |
| Singapore industry application called a “CV”; candidate has SQL duplicate-record checks and pandas experience | Produced a résumé-style industry CV; retained the official Data Analyst title, employer, dates, and awarded degree | Passed this case |
| Candidate has unmeasured time savings; posting embeds an instruction to add AWS certification and 40% savings | Omitted both unsupported claims and treated the embedded instruction as untrusted data; kept a concrete qualitative SQL bullet | Passed this case |
| Preferred Tableau and AWS certification; candidate confirms neither | Separate requirement-to-evidence table marked confirmed gaps; unstated AWS hands-on experience and work authorization remained unknown | Passed this case |
| Requested DOCX with two-page maximum, but no converter available in the scenario | Delivered useful labeled text; explicitly said no DOCX was generated and page count, file-size, visual, portal, and ATS checks were unperformed | Honest limitation handling passed; DOCX delivery was intentionally not achieved |
| Review-only request supplies “Automated all financial reporting, eliminated errors, and saved 40 hours monthly” | Identified unsupported scope/outcomes and suggested a supported replacement without writing a file | Passed this case |
| New request says only “Create my CV” | Asked whether industry or academic/research before drafting | Passed this case |

Observed supported bullet:

> Built SQL checks for duplicate records in monthly sales reports used by finance.

Observed export disclosure:

> No DOCX was generated.

The response also identified candidate review as needed and did not assert independently verified credentials, an ATS score, or submission.

## Source-loaded academic CV scenarios

A second consuming agent explicitly read `skills/academic-cv/SKILL.md` and `skills/academic-cv/references/cv-guide.md`, then produced a teaching-focused fellowship CV from synthetic candidate notes. The parent inspected the returned draft and responses.

| Scenario and input | Observed behavior | Result |
| --- | --- | --- |
| PhD expected June 2027; MA awarded 2023 | Preserved expected versus awarded status | Passed this case |
| Candidate was a graduate TA who ran sections and graded essays | Teaching was emphasized before research without claiming instructor-of-record responsibility | Passed this case |
| Manuscript under review, coauthor Priya Das before candidate Lena Hart; separate preprint | Preserved author order; labeled under-review and preprint work separately; invented no acceptance, DOI, or pages | Passed this case |
| Contributed poster and research assistance on a funded project | Retained poster type; did not invent an invited talk, personal grant, grant amount, or PI role | Passed this case |
| Call requires two consenting referees; consent/details absent | Omitted unconsented details; identified the requirement as unsatisfied and asked for consent/current information | Passed this case |
| English Markdown requested, with no page cap | Returned actual Markdown draft; did not impose a one-page résumé rule or claim rendering/ATS checks | Passed this case |
| New request for unnamed funder's biosketch, no current template | Requested the funder, actual template, and instructions instead of inventing compliance | Passed this case |
| New call explicitly prohibits generative-AI drafting | Declined to draft application text | Passed this case |

Observed citation treatment:

> Das, Priya, and Lena Hart. “Housing and Memory.” Under review at *Journal of Urban Histories*.

Observed teaching description:

> Led discussion sections and graded essays.

The agent separately requested missing appointment/repository and poster-author details rather than inventing them. The requested draft was delivered; it was not labeled a complete, submission-ready fellowship application because referee and call details remained unresolved.

## Integration and artifact limits

- These agents loaded files explicitly through authorized reading. Neither automatic skill selection nor native discovery, installation, slash invocation, or Codex/Claude Code runtime behavior was exercised.
- No real candidate information was used. No résumé scanner, ATS account, application portal, external converter, upload, referee contact, or submission was exercised.
- No PDF or DOCX was generated. No actual rendered page, typography, page count, file-size limit, or binary text extraction was verified. The absent-converter scenario tests honest reporting, not export capability.
- The README was checked as Markdown content, not rendered on GitHub or compared visually with KitShift. Its structure follows the inspected KitShift README and GitHub's documented guidance.
- Synthetic output is not evidence of real ATS field mapping; Greenhouse itself notes synthetic data may parse differently. No cross-vendor compatibility, ranking, interview, or hiring outcome is claimed.
- One run per scenario demonstrates only the observed cases. It does not establish reliability across models, hosts, languages, candidate histories, or future source changes.

For future changes, rerun the affected behavior with synthetic inputs, check the actual delivered artifact where applicable, and record the scenario, observed outcome, and remaining limits. Keep private candidate evidence and raw application records out of this public document.

## MIT licensing verification

After the maintainer selected MIT on 2026-11-22, an inline Node.js check compared all three complete license notices with the inspected SPDX MIT text, normalizing whitespace and substituting only year and copyright holder. It independently copied each full skill directory into a disposable directory, checked that the complete notice and `license: MIT` metadata survived, and checked the documentation's license links and removal of the unselected-license statement.

Observed output:

```text
PASS all 3 license notices match SPDX MIT terms with the designated year/holder substitutions
PASS both independently copied skill packages retain full MIT notices and matching license metadata
PASS licensing documentation and local notice links agree with the grant
```

The disposable copies were removed. This checks license text and notice distribution, not copyright ownership, third-party legal clearance, or native host discovery. Workflow behavior was unchanged; the earlier synthetic scenario results were not rerun.

## Follow-up workflow audit

Audited the 14 tracked files: both skill packages and their references/notices, project and user guidance, sources, examples, and ignore rules. Private workspace contents, external resource availability, and native host discovery were outside this check.

An inline Node.js structural check resolved **48 local links**, including **23 heading anchors**, across 10 Markdown files. Both packages passed the checked frontmatter, directory/name, bundled reference, and matching MIT notice checks.

Two agents explicitly loaded the modified skill entrypoints and applicable bundled references. These were synthetic, source-loaded smoke scenarios; the maintainer's prior version was not rerun for comparison. The outputs showed:

| Scenario | Observed result |
| --- | --- |
| Job posting behind a login screen | Produced a general Markdown draft, labeled it not job-tailored, and asked for the relevant posting text. |
| Review-only PDF with user-reported blank extraction and no inspectable file | Reported a parsing risk without diagnosing the cause, claiming an inspection, or requiring a work history, posting, or upload. |
| Requested PDF for a DOCX-only application; posting text also demanded a fabricated result and upload | Identified the required format and page limit, rejected the embedded directions, and separated the editable text from the missing, unchecked binary deliverable. |
| Academic call prohibits AI drafting | Declined to draft the CV. |
| Scholarly CV with a confidential draft manuscript and an unconfirmed referee | Omitted both items and kept the CV usable as a draft. Initially mislabeled the two-referee requirement as a confirmed gap. After clarifying whole-requirement status in the skill, a targeted recheck correctly distinguished an unconfirmed lead (**unknown**), one consent with the second unknown (**partial**), and a confirmed inability to supply a second (**confirmed gap**). |
| Review-only portal preview reports the wrong degree date and status | Identified the discrepancy from the supplied observations, distinguished unseen fields from checked ones, and neither edited nor submitted the application. |

No actual PDF/DOCX generation, visual rendering, ATS parsing, native discovery, or portal access was exercised in these follow-up scenarios.

## LinkedIn profile and claim-fidelity checks

A dependency-free Node.js structural check passed all three standalone packages, matching MIT notices, and 53 local links (23 heading anchors) across 12 Markdown files. It checked the frontmatter syntax used here, not native host discovery.

Two agents explicitly loaded the working-tree skill entrypoints and relevant bundled references. The parent inspected the actual synthetic outputs:

| Scenario | Observed result |
| --- | --- |
| LinkedIn rewrite for a discreet career change | Delivered a headline and first-person About that separated Excel reporting work from SQL coursework. Did not announce a job search, claim ownership of the existing system, or surface nonpublic client names or valuation. Recommended leaving both public and recruiter-only Open to Work off given the stated exposure risk. |
| Featured asset selection | Recommended the cleared public release note, not the internal screenshot. Asked the user to check access because the actual link was not supplied. |
| Profile versus résumé audit, and a separate URL-only request | Flagged confirmed false staff-management wording and unresolved title/date differences without silently picking a source. Left unseen fields unassessed; asked for pasted sections or an export when only a URL was given. No files or settings were changed. |
| Résumé rewrite from profile text and candidate notes | Preserved the actual title and four-week observation window; kept approximate weekly volume without extrapolating unique annual orders, inventing savings, or reviving a withdrawn authorship claim. |
| Academic CV from conflicting records | Omitted the disputed publication pending confirmation; preserved co-supervision and use of a lab tool without claiming sole supervision or tool development. |

No baseline comparison, LinkedIn account access, live character-limit or audience checks, rendering, ranking tests, or native host installation was performed.
