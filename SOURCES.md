# Research and sources

Research checked **2026-11-22**. Scope: industry résumés, academic CVs, ATS-conscious document preparation, reusable Agent Skills, and this repository's README. This is an evidence synthesis, not an evaluation of hiring outcomes or legal advice. Links are live, mutable sources, not version-pinned snapshots.

## Findings that drive the design

| Question | Evidence and limitation | Project decision |
| --- | --- | --- |
| Is there one “Harvard standard”? | Harvard College gives résumé advice; GSAS explicitly says there is no single best CV format and to follow the field. [H1](#h1-harvard-college-résumé-guide), [H2](#h2-harvard-gsas-cv-guide) | Say **Harvard-informed**, not Harvard-approved, certified, or a universal standard. |
| Is a CV just a longer résumé? | GSAS covers scholarly accomplishments, publications, research, teaching, and references. Industry documents called “CVs” can have a different purpose. [H2](#h2-harvard-gsas-cv-guide), [U1](#u1-berkeley-academic-cv-elements) | Separate industry résumé and academic-CV skills; clarify ambiguous terminology by audience. |
| Must every bullet have a metric or XYZ formula? | Harvard recommends active, specific, fact-based writing and demonstrated results, but does not require a number or named formula for every bullet. [H1](#h1-harvard-college-résumé-guide) | Use evidence-backed action/context/contribution/outcome writing; accept qualitative evidence. |
| Can AI author everything? | Harvard says to begin with candidate material, use AI suggestions critically, retain authenticity, and not use AI as the primary author. [H3](#h3-harvard-ai-guidance) | Work from candidate-authored facts and obtain review; don't market AI output as Harvard-compliant authorship. |
| Are columns and tables always unreadable? | Greenhouse lists columns, complex tables, text boxes, headers/footers, images, and inconsistent sections as failure risks. [A1](#a1-greenhouse-parsing) | Use single-column body text as a conservative default, not a universal parser law. |
| Is PDF always the right choice? | Greenhouse accepts several formats; Harvard says to check PDF conversion. Neither establishes a universally preferred format. [A2](#a2-greenhouse-uploads), [H1](#h1-harvard-college-résumé-guide) | Follow application instructions; inspect the actual requested PDF or DOCX. |
| Does upload acceptance prove parsing? | Greenhouse documents up to 100 MB for uploads but a 2.5 MB résumé parsing limit. [A1](#a1-greenhouse-parsing), [A2](#a2-greenhouse-uploads) | Distinguish upload, extraction, field mapping, screening, and selection. Recheck applicable limits before relying on them. |
| Is ATS “just a database,” with no automatic rejection? | Greenhouse documents employer-configured rejection rules for application-question responses. [A3](#a3-greenhouse-auto-reject) | Explain workflow variability; don't promise a keyword rewrite can overcome eligibility rules. |
| Are there universal ATS scores or pass thresholds? | Reviewed primary sources do not establish a cross-vendor score, keyword density, or rejection percentage. This absence does not prove no product offers matching/ranking. | No invented match percentages, “100% ATS compatible,” or rejection statistics. |
| Is text extraction an ATS test? | A local extractor does not exercise a vendor's parser, configuration, ranking, or decision process. This is a verification-method distinction, not a measured cross-vendor result. | Report it as text extraction only; verify rendered pages separately. |
| Should all locales omit a photo? | Harvard's US-focused guide says no picture; Europass suggests a photograph. [H1](#h1-harvard-college-résumé-guide), [U2](#u2-europass-cv-guidance) | Resolve destination and instructions; no photo or sensitive demographic details by default, and no blanket claims about Europe. |

## Primary career sources

### H1. Harvard College résumé guide

[Harvard College Guide to Creating a Strong Resume](https://careerservices.fas.harvard.edu/resources/create-a-strong-resume/), Harvard FAS Mignone Center for Career Success.

Read the page's substantive guidance. Supports concise, specific, active, factual language; results; consistent formatting; headings by importance; reverse chronology; US-focused personal-information advice; and country variation. Does not establish the example repository's exact typography, required skills-first ordering, mandatory XYZ, or universal PDF preference. Applied in the résumé writing guide and evidence boundaries.

### H2. Harvard GSAS CV guide

[GSAS CV & Cover Letter Guide](https://careerservices.fas.harvard.edu/resources/gsas-cv-cover-letter-guide-2/), Harvard FAS Mignone Center for Career Success.

Read the page's CV instructions. Supports academic purpose, flexible field-specific structure, strategic ordering, an archival versus targeted CV, common typography, 10–12 pt text, equal 0.75–1 inch margins, and a contextual two-to-five-page observation for graduate students. No universal academic-CV page limit. Applied in `academic-cv`. Publication-status rules are attributed to Berkeley below, not inferred from this page's samples.

The linked GSAS sample PDF could not be retrieved by the research agent (HTTP 404). No sample-PDF visual or typography inspection is claimed. Neither skill reproduces a Harvard template.

### H3. Harvard AI guidance

[AI for Resumes and Cover Letters](https://careerservices.fas.harvard.edu/ai-resumes-and-cover-letters/), Harvard FAS Mignone Center for Career Success.

Read the page. Supports starting from candidate material, critical review of suggested edits, authentic voice, basic ATS-conscious formatting, explicitly listing skills and job keywords in context, and privacy caution. It also says application instructions can restrict AI use. Applied in both skills. This project must not override an employer's AI-use rules.

### U1. Berkeley academic CV elements

[The CV — Part 2: Elements](https://career.berkeley.edu/grad-students-postdocs/academic-job-search/the-cv-part-2-elements/), UC Berkeley Career Engagement.

Read the page. Supports modular sections and field review, bibliographic conventions, author order, distinguishing teaching responsibility, academic references, submitted/in-progress categories, and reserving “forthcoming” for accepted work. Applied in the academic CV guide. Its academic reference-sheet advice is not carried over to industry résumés.

### U2. Europass CV guidance

[Create your Europass CV](https://europass.europa.eu/en/create-europass-cv), European Commission / Europass.

Read the page. Supports tailoring to a vacancy, clear active language, reverse chronology, and an example of locale-specific photo advice that differs from Harvard. Not proof that Europass or photographs are required across Europe. Used to make locale a consequential input, not a US-only assumption.

### U3. Europass personal information

[Managing your personal information in Europass](https://europass.europa.eu/en/about-europass/protection-your-personal-data/personal-information).

Read the page. Discusses control over sharing and avoiding sensitive personal information. Informs cautious data handling; it does not establish that local Git ignores, an AI host, or this package provides encryption or isolation.

## Primary ATS sources

### A1. Greenhouse parsing

[Unsuccessful resume parse](https://support.greenhouse.io/hc/en-us/articles/200989175-Unsuccessful-resume-parse).

Read the article. Supports documented formatting risks, a stated 2.5 MB parsing limit, and the difference between a résumé attachment and successful field population. It also notes synthetic/fake data can parse differently. Used for conservative defaults and honest verification labels, not universal guarantees.

### A2. Greenhouse uploads

[Supported formats for resumes, cover letters and other candidate uploads](https://support.greenhouse.io/hc/en-us/articles/360052218132-Supported-formats-for-resumes-cover-letters-and-other-candidate-uploads).

Read the article. Lists DOC, DOCX, PDF, RTF, and TXT and a 100 MB upload limit. Contrasted with A1 rather than conflating acceptance and parsing. These values are product-specific and mutable.

### A3. Greenhouse auto-reject

[Auto-reject](https://support.greenhouse.io/hc/en-us/articles/360000653472-Auto-reject).

Read the article. Documents automatic rejection based on configured answers to Yes/No, single-select, and multi-select application questions. It does not establish automatic rejection from résumé formatting or a universal scoring model.

### A4. Lever: access limitation

[Understanding Resume Parsing](https://help.lever.co/hc/en-us/articles/20087345054749-Understanding-resume-parsing) and [Adding and deleting resumes](https://help.lever.co/hc/en-us/articles/20087357076253-Adding-and-deleting-resumes).

The research agent located official search excerpts; direct retrieval failed, including an independently observed HTTP 401 for the parsing page. Treat this as incomplete evidence. Exact Lever formats/limits are deliberately not used as normative skill rules. No claim of verified Lever compatibility is made.

## Existing projects compared

These are implementation examples, not authoritative evidence for hiring outcomes. Inspected documents are noted; their software was not installed, executed, or security-audited. Recommendations below are this project's design judgments, not measured effectiveness rankings.

| Project | Inspected evidence | Useful pattern | Not carried forward |
| --- | --- | --- | --- |
| [dabydat/resume-builder-skill](https://github.com/dabydat/resume-builder-skill) | README and [SKILL.md](https://github.com/dabydat/resume-builder-skill/blob/HEAD/skill/SKILL.md) | Separate references for writing, layout, ATS, and pitfalls; concrete workflow | Mandatory dual export, universal PDF/ATS claims, broad triggers, exact font rules labeled Harvard; examples' domain detail must not become candidate claims without evidence |
| [darkseidH/resume-tailor-skill](https://github.com/darkseidH/resume-tailor-skill) | README and [SKILL.md](https://github.com/darkseidH/resume-tailor-skill/blob/main/SKILL.md) | Claim provenance, private workspace, honest gaps, factual versus export checks | Mandatory profile map, persistent onboarding and publishing state, fixed renderer dependency, approval of every profile update as a prerequisite to unrelated drafting |
| [agentheath/resume-tailor-pro](https://github.com/agentheath/resume-tailor-pro) | README and accuracy/ATS/title-tailoring sections of [SKILL.md](https://github.com/agentheath/resume-tailor-pro/blob/master/SKILL.md) | Candidate facts constrain keyword adaptation; keep private profile material separate | Unsupported universal parser-scoring assertions, mandatory past tense, rewriting historical titles to a target title, automatic dependency installation |
| [RenderCV](https://github.com/rendercv/rendercv) and [its skill](https://github.com/rendercv/rendercv-skill) | Project README's usage/skill sections, skill README, and [SKILL.md](https://github.com/rendercv/rendercv-skill/blob/main/skills/rendercv/SKILL.md) introduction/schema excerpt | Structured input and an explicit rendering workflow as an optional tool choice | A bundled renderer, required dependencies, automatic installation, or treating a theme named `harvard` as university endorsement; no independent validation of its output claims |

No upstream skill body, code, document template, or sample résumé has been vendored. These packages are independently written instruction syntheses; external links and research do not transfer a source's license or endorsement to this repository. No copyright or licensing audit of the compared projects is claimed.

## LinkedIn and workflow comparison

The following projects are research references, not managed dependencies. The links pin the repository heads resolved during review. No upstream text, templates, scoring tools, or executable code were imported.

| Project and inspected sources | Workflow decision |
| --- | --- |
| Remotivated/job-hunt-skills: [LinkedIn optimizer](https://github.com/Remotivated/job-hunt-skills/blob/51e827c5850ae61c6129c4c2888f242ffcf84535/plugins/job-hunt-skills/skills/linkedin-optimizer/SKILL.md), [claim check](https://github.com/Remotivated/job-hunt-skills/blob/51e827c5850ae61c6129c4c2888f242ffcf84535/plugins/job-hunt-skills/skills/claim-check/SKILL.md), [résumé auditor](https://github.com/Remotivated/job-hunt-skills/blob/51e827c5850ae61c6129c4c2888f242ffcf84535/plugins/job-hunt-skills/skills/resume-auditor/SKILL.md) | Explicit final claim checks and actionable, section-specific findings. Do not require saved state, a standalone audit skill, fixed variant counts, pinned-skill ranking assumptions, or mandatory report files. |
| Paramchoudhary/ResumeSkills: [quantifier](https://github.com/Paramchoudhary/ResumeSkills/blob/74ae19e7c62b0516d1c298328e5544976c12da5d/skills/resume-quantifier/SKILL.md), [career transitions](https://github.com/Paramchoudhary/ResumeSkills/blob/74ae19e7c62b0516d1c298328e5544976c12da5d/skills/career-changer-translator/SKILL.md), [profile optimizer](https://github.com/Paramchoudhary/ResumeSkills/blob/74ae19e7c62b0516d1c298328e5544976c12da5d/skills/linkedin-profile-optimizer/SKILL.md) | Ask about measurable scope and map demonstrated transferable work within `resume-writing`. Do not turn guesses into lower bounds, substitute target titles, or repeat unsupported ranking, profile-view, and screening claims. |
| yanliudesign/offer-toolkit-skill: [résumé workflow](https://github.com/yanliudesign/offer-toolkit-skill/blob/3b85d2e1b8363bbd6dab06866641bdc6e61071df/resume-skill/SKILL.md), [LinkedIn intake](https://github.com/yanliudesign/offer-toolkit-skill/blob/3b85d2e1b8363bbd6dab06866641bdc6e61071df/resume-skill/prompts/linkedin-import.md) | Accept pasted profile text or a user-provided local export and validate content before formatting. Do not fetch profile URLs, assume PDF completeness, import the HTML template gallery, or equate print optimization with ATS compatibility. |
| borghei/Claude-Skills: [LinkedIn profile optimizer](https://github.com/borghei/Claude-Skills/blob/25bf86b89c6c1e63f433a5b65e8cfcb6cf0b7ad3/tools/linkedin/linkedin-profile-optimizer/SKILL.md) | An offline, audience-first editorial workflow with explicit unassessed sections is useful. Its skill declares `MIT + Commons Clause`; no material was copied or adapted for redistribution. Its numeric rules, CLI tooling, and score thresholds were not adopted. |

### Primary LinkedIn sources

- [LinkedIn profile tip sheet](https://socialimpact.linkedin.com/content/dam/me/socialimpact-linkedin-com/lifg-resources/linkedin-training-content/linkedin-profile-tip-sheet.pdf): the extracted text supports first-person About, specific Experience, skill context, and work samples. It was not used to infer UI behavior or ranking.
- [Recruiter search filters](https://www.linkedin.com/help/recruiter/answer/a414428) and [Featured FAQ](https://www.linkedin.com/help/linkedin/answer/a553419): titles and skills are documented filter inputs; Featured is not discoverable through search and viewing is subject to sign-in and visibility conditions. Neither supports a ranking formula or score.
- [Save a profile as a PDF](https://www.linkedin.com/help/linkedin/answer/a541960) and [User Agreement §8](https://www.linkedin.com/legal/user-agreement#dos): desktop export has availability and language limitations; use user-supplied material rather than scraping or circumventing access restrictions. Export completeness was not measured.
- [Open to Work](https://www.linkedin.com/help/linkedin/answer/a507508), [public profile controls](https://www.linkedin.com/help/linkedin/answer/a528138), and [share profile updates](https://www.linkedin.com/help/linkedin/answer/a529062): recruiter-only visibility is not guaranteed private, public-profile indexing can lag, and notifications are distinct from the visibility of saved edits. Do not assume every account, locale, or interface has the same settings or text limits.

No account, live profile, search ranking, or settings were tested. The package is independently authored guidance for manual publishing.

## Project licensing

The maintainer selected **MIT** for this project's original skills and documentation. The full grant is in [LICENSE](LICENSE), with identical notices bundled in [resume-writing](skills/resume-writing/LICENSE), [academic-cv](skills/academic-cv/LICENSE), and [linkedin-profile](skills/linkedin-profile/LICENSE). The copyright notice follows the maintainer's established KitShift convention: `Copyright (c) 2026 rizariaputrawira`; this project's original material was created in 2026.

The legal text was checked against the [SPDX MIT record](https://spdx.org/licenses/MIT.html) and [Open Source Initiative's MIT text](https://opensource.org/license/mit). Required copyright and permission notices must accompany copies or substantial portions. The grant applies to this project's original material, not external websites, linked templates, third-party projects, or candidate-supplied records. Existing source attributions and access limitations above remain applicable.

## Packaging and README sources

- [Agent Skills specification](https://agentskills.io/specification): required `SKILL.md`, `name`/`description` frontmatter, directory/name agreement, relative supporting references, progressive disclosure. Packaging guidance, not evidence of native discovery or agent compliance.
- [OpenAI's build-skills guidance](https://learn.chatgpt.com/docs/build-skills): current documented Codex skill locations and explicit invocation. Documentation was read; no Codex runtime installation was tested.
- [Claude Code skills documentation](https://code.claude.com/docs/en/skills): current documented skill locations and invocation. Documentation was read; no Claude Code runtime installation was tested.
- [Cursor Agent Skills](https://cursor.com/docs/skills) and [VS Code Agent Skills](https://code.visualstudio.com/docs/agent-customization/agent-skills): documented discovery directories and invocation for the hosts listed in the README; no runtime tests on these clients.
- [GitHub README guidance](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes): explain purpose/value, getting started, help and maintainers; prefer relative links to repository files and clear headings.
- [KitShift README](https://github.com/rizariaputrawira/KitShift): structure requested by the repository owner. Inspected the local sibling checkout's opening sections and heading hierarchy. Adapted its answer-first introduction, navigation, capabilities, quick start, how-it-works, safety/privacy, verification/limits, help, and sources organization—not its runtime settings, installers, support claims, or skill inventory. No rendered GitHub-page comparison was performed.

## Evidence limits and maintenance

This research does not establish a single global CV standard, a cross-vendor ATS certification, quantified hiring improvements, or compliance with every employer's AI policy. Primary web text was sufficient for the claims above; linked document samples were not visually validated. Comparative project claims remain those projects' claims unless supported independently.

Recheck the owning source before changing an evidence-backed rule. Keep vendor facts separate from project defaults and preserve contradictions, dates, inaccessible evidence, and actual verification results. See [verification](docs/verification.md) for this project's observed package and scenario checks.
