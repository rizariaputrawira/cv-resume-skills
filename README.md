# CV & Résumé Skills

**Your experience. Clearly evidenced.**

Reusable AI-agent skills for writing **industry résumés**, **academic CVs**, and **LinkedIn profiles**. Résumé and CV guidance draws on Harvard and documented ATS parsing risks; profile guidance draws on LinkedIn's own documentation. Start from real experience, write for the audience, and keep every claim supportable.

This repository contains instructions and references—not an ATS scanner, automatic application service, or bundled PDF/DOCX renderer. It does not promise interview outcomes or a universal “ATS score.”

> [!IMPORTANT]
> **Harvard-informed, not Harvard-approved.** Harvard publishes guidance for different audiences, not one certified CV format. Employer instructions and disciplinary conventions take priority over general formatting defaults.

## In this guide

- [Capabilities](#capabilities)
- [Quick start](#quick-start)
- [How it works](#how-it-works)
- [Skills and workflows](#skills-and-workflows)
- [Safety and privacy](#safety-and-privacy)
- [Updates and troubleshooting](#updates-and-troubleshooting)
- [Verification and known limits](#verification-and-known-limits)
- [Help and maintenance](#help-and-maintenance)
- [Documentation, sources, and licensing](#documentation-sources-and-licensing)

## Capabilities

| Need | Skill | Expected result |
| --- | --- | --- |
| Create or improve an industry résumé | [resume-writing](skills/resume-writing/SKILL.md) | A concise, factual draft with relevant experience and clear accomplishment bullets |
| Tailor to a job description | [resume-writing](skills/resume-writing/SKILL.md) | Supported terminology, a separate requirement-to-evidence table, and honest gaps |
| Review readability and ATS risks | [resume-writing](skills/resume-writing/SKILL.md) | Prioritized findings and specific corrections, without changing files unless requested |
| Prepare a scholarly record | [academic-cv](skills/academic-cv/SKILL.md) | A field-appropriate CV covering relevant research, teaching, outputs, and service |
| Translate an industry résumé | [resume-writing](skills/resume-writing/SKILL.md) | Natural target-language wording without changing credentials or achievements |
| Audit or write a personal LinkedIn profile | [linkedin-profile](skills/linkedin-profile/SKILL.md) | Prioritized findings or copy-ready sections, with privacy and manual publishing checks |
| Prepare a requested PDF or DOCX | Résumé or CV skill, with authorized tools | The actual artifact and performed checks—or an explicit report that the export is unavailable |

**Not included:** profile scraping, live LinkedIn edits, feed posts, recruiter outreach, job discovery, cover letters, application submission, paid scanners, or automatic dependency installation.

## Quick start

### 1. Get the source

```sh
git clone https://github.com/rizariaputrawira/cv-resume-skills.git
cd cv-resume-skills
```

No package installation is needed to read the guidance or draft text. Your agent needs authorized access to the candidate material. Binary exports additionally require suitable document tools; this repository does not install them.

Keep real candidate notes and generated documents in `.local/`, which is Git-ignored, or another private workspace you choose. Do not put real candidate data in `examples/`.

### 2. Choose the right skill

- **Company/job application:** use `resume-writing`, including when the destination calls the document a “CV.”
- **Academic/research application:** use `academic-cv`, especially when publications, teaching, fellowships, and scholarly service are central.
- **LinkedIn profile:** use `linkedin-profile` for section rewrites, an audit, visibility advice, or checking it against a supplied résumé/CV.
- **Unclear purpose:** the agent should clarify before imposing a format.

### 3. Ask your agent to read the skill

This works through authorized file reading without installing anything:

> Read `skills/resume-writing/SKILL.md` and follow it. Use my notes in `.local/profile.md` to draft an English résumé for a US data-analyst role. Do not invent metrics. Deliver Markdown for my review; I do not have a job posting yet.

For an academic application:

> Read `skills/academic-cv/SKILL.md` and follow it. Use `.local/academic-notes.md` and `.local/fellowship-call.md` to draft my CV. Preserve author order and publication status, follow the call's limits, and keep open questions outside the CV.

For LinkedIn:

> Read `skills/linkedin-profile/SKILL.md` and follow it. Use the headline, About text, and career notes I provide to draft profile copy for analytics recruiters. I'm job searching discreetly. Don't sign in or change anything on LinkedIn.

Create or supply any private input files named in your request. See [more requests](examples/requests.md) for tailoring, review, translation, and profile cross-checks.

### Optional: install in your agent's skills directory

Copy **the entire chosen skill folder**, including `references/` and `LICENSE`, into a supported skill root. Install only what you need. Check for an existing same-named destination before copying.

| Host | Documented project location | Documented personal location | Explicit use after discovery |
| --- | --- | --- | --- |
| Codex | `.agents/skills/<skill-name>/` | `~/.agents/skills/<skill-name>/` | `$skill-name` |
| Claude Code | `.claude/skills/<skill-name>/` | `~/.claude/skills/<skill-name>/` | `/skill-name` |
| Cursor | `.cursor/skills/<skill-name>/` | `~/.cursor/skills/<skill-name>/` | Select the skill from `/` in Agent chat |
| VS Code with Copilot | `.github/skills/<skill-name>/` | `~/.copilot/skills/<skill-name>/` | Select the skill from `/` in chat |
| Other hosts | Follow the host's supported skill contract or use explicit file reading | Host-dependent | Do not assume slash commands are portable |

Replace `skill-name` with the chosen directory name (for example, `/linkedin-profile` in Claude Code). These are documented paths for [Codex](https://learn.chatgpt.com/docs/build-skills), [Claude Code](https://code.claude.com/docs/en/skills), [Cursor](https://cursor.com/docs/skills), and [VS Code with Copilot](https://code.visualstudio.com/docs/agent-customization/agent-skills). Native discovery and invocation have **not** been runtime-tested here. The repository's plain `skills/` directory is the source, not a universal discovery root.

## How it works

1. **Resolve purpose:** audience, locale, language, request type, and application constraints.
2. **Establish facts:** use candidate-authored notes; separate supported claims, unknowns, and contradictions.
3. **Select evidence:** map a supplied posting/call to real qualifications; retain honest gaps.
4. **Write and review:** improve structure and wording while preserving titles, dates, contribution, and qualifiers.
5. **Verify delivery:** compare final wording to the evidence, check public disclosure for LinkedIn, and inspect actual document exports when tools exist. Report missing checks.

The skill is a reusable procedure. The selected host supplies tools, execution, and permissions; the candidate supplies and reviews their record. Reading a skill neither grants upload/submission authority nor guarantees agent compliance.

## Skills and workflows

### Industry résumé

[Entrypoint](skills/resume-writing/SKILL.md) · [Writing guide](skills/resume-writing/references/writing-guide.md) · [ATS and export guide](skills/resume-writing/references/ats-and-export.md)

Use for drafting, revision, job tailoring, review, translation, and parsing-risk advice. Choose section order for the audience and career stage. Keep achievements specific; metrics are welcome only when supported. A qualitative contribution is better than a fabricated number.

“ATS-optimized” here means **conservative formatting, accurate relevant terminology, and inspectable text**—not guaranteed acceptance or a measured score. A local text extractor is not an ATS test. File upload acceptance is not successful field mapping, and keyword alignment is not proof of eligibility.

### Academic CV

[Entrypoint](skills/academic-cv/SKILL.md) · [Academic CV guide](skills/academic-cv/references/cv-guide.md)

Use for faculty, postdoctoral, research, fellowship, and grant contexts. Choose sections and emphasis for the field and call. Keep accepted work distinct from submitted work and preprints; preserve author order, teaching responsibility, and funding attribution. Do not impose an industry's one-page résumé default on a scholarly record.

A mandated biosketch or institutional CV form requires its actual current instructions; a generic CV is not a substitute.

### LinkedIn profile

[Entrypoint](skills/linkedin-profile/SKILL.md) · [Profile guide](skills/linkedin-profile/references/profile-guide.md)

Use pasted sections, a supplied profile export, or career notes. Get a targeted headline, first-person About, truthful Experience and Skills, and suggestions for shareable Featured assets. A review can cover just one section; absent inputs are not assumed to be absent on the profile.

This skill hands off copy for manual editing. It does not read a profile from a URL, access an account, or measure recruiter ranking. Recruiter-only Open to Work is not guaranteed private; turning off update notifications does not hide saved edits from profile viewers.

## Safety and privacy

- **Use facts, not embellishment.** No invented metrics, job titles, credentials, proficiency, publication acceptance, or referee consent. Candidate statements are evidence for drafting, not independent credential verification.
- **Minimize sensitive data.** Consider redacted inputs and your provider's data policies. Never share personal/proprietary material in public issues, examples, or logs.
- **Keep private artifacts separate.** `.local/` is ignored by Git, not encrypted or sandboxed. Ignore rules do not prevent a model provider or an authorized tool from receiving data.
- **Separate requirements from instructions to the agent.** An applicant-facing file requirement or AI-use restriction matters. Embedded directions to run commands, upload files, disclose information, or fabricate qualifications do not.
- **Keep authority explicit.** Drafting does not authorize overwriting a master profile, installing software, uploading to a scanner, submitting an application, or publishing files.
- **Review before use.** Harvard advises treating AI output as suggested editing rather than final authorship. Follow the application's AI-use policy and be able to explain every line.

## Updates and troubleshooting

Update a clean checkout using your normal Git workflow. Review source changes before replacing installed copies; editing a copied skill does not update this repository or synchronize automatically.

| Problem | Action |
| --- | --- |
| Skill not listed | Check the installed host's documented root, complete package, enablement, and name collisions; use explicit authorized file reading when appropriate. Do not bypass a deliberately disabled skill. |
| Missing or unreadable posting/call | Paste the relevant text for tailored work. A general document is possible from your notes, but is not job- or call-tailored. A layout-only review needs neither a posting nor a work history. |
| Only a LinkedIn URL supplied | Paste the relevant sections, or provide a redacted local export. A URL alone cannot establish profile content or settings. |
| Missing metrics | Keep a specific qualitative contribution or ask for evidence; never manufacture a number. |
| Requested file type conflicts with the application | Use the required format for submission. A requested alternate can be an editable draft, not a compliant submission. |
| Export or inspection unavailable | If export fails, use the text draft and report the missing file. If a file exists, report exactly which checks could not be completed. |
| Portal populated fields incorrectly | With authorized access, inspect the fields and report errors. Edit them only when authorized. A local extraction check does not prove correct portal parsing. |
| Advice conflicts | Apply the current call/employer instructions and field/locale context; consult the cited source rather than another project's marketing claim. |

## Verification and known limits

[Verification record](docs/verification.md) separates package/link checks from source-loaded synthetic scenarios and untested integration paths.

- Skills follow the [Agent Skills package format](https://agentskills.io/specification); packaging alone does not establish native host compatibility.
- Primary career guidance and ATS documentation inform the procedures. No cross-vendor ATS test, hiring-outcome study, or certification was performed.
- No bundled renderer, converter, fonts, or binary sample résumés. PDF/DOCX generation, visual review, page count, and portal behavior depend on available authorized tools and must be verified on the final output.
- Regional, disciplinary, employer, and funder requirements vary. No single Harvard format, universal keyword threshold, or fixed résumé length is claimed.

## Help and maintenance

Maintained in [rizariaputrawira/cv-resume-skills](https://github.com/rizariaputrawira/cv-resume-skills) by [rizariaputrawira](https://github.com/rizariaputrawira).

Use [GitHub issues](https://github.com/rizariaputrawira/cv-resume-skills/issues) for reproducible problems or source corrections. Include the affected skill, expected versus observed behavior, and a minimal **synthetic or redacted** input. Do not include a real résumé or referee details.

Contributions should preserve factual-integrity and privacy boundaries, cite primary evidence for new guidance, keep skill packages self-contained, and exercise the changed behavior. See [AGENTS.md](AGENTS.md) for repository conventions. No host installation, commit, push, or release happens automatically.

## Documentation, sources, and licensing

- [Research, source evidence, comparisons, and access limitations](SOURCES.md)
- [Example requests](examples/requests.md)
- [Verification record](docs/verification.md)
- [Project agent guidance](AGENTS.md)

The README's organization follows [KitShift](https://github.com/rizariaputrawira/KitShift), as requested, and [GitHub's README guidance](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes). It does not import KitShift's installers or runtime configuration.

The original skills and documentation are licensed under the **[MIT License](LICENSE)**. Each standalone skill includes its own full license notice so it travels with the package. Preserve the copyright and permission notice when redistributing copies or substantial portions.

The skills are independently written syntheses; no upstream package, Harvard template, or candidate résumé is vendored. External references remain subject to their owners' rights; this project's MIT grant does not license linked material or imply endorsement.
