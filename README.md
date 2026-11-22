# CV & Résumé Skills

**Your experience. Clearly evidenced.**

Reusable AI-agent skills for writing **industry résumés** and **academic CVs**, informed by Harvard career guidance and documented ATS parsing risks. Start from your own experience, tailor it to the audience, and keep every claim supportable.

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
| Prepare a requested PDF or DOCX | Either, with available authorized tools | The actual artifact and performed checks—or an explicit report that the export is unavailable |

**Not included:** job discovery, cover letters, LinkedIn editing, recruiter outreach, application submission, paid scanners, dependency auto-installation, or model/host configuration.

## Quick start

### 1. Get the source

```sh
git clone https://github.com/rizariaputrawira/cv-resume-skills.git
cd cv-resume-skills
```

No package installation is needed to read the guidance or draft text. Your agent needs authorized access to the candidate material. Binary exports additionally require suitable document tools; this repository does not install them.

Keep real candidate notes and generated documents in `.local/`, which is Git-ignored, or another private workspace you choose. Do not put real candidate data in `examples/`.

### 2. Choose the right document

- **Company/job application:** use `resume-writing`, including when the destination calls the document a “CV.”
- **Academic/research application:** use `academic-cv`, especially when publications, teaching, fellowships, and scholarly service are central.
- **Unclear purpose:** the agent should clarify before imposing a format.

### 3. Ask your agent to read the skill

This works through authorized file reading without installing anything:

> Read `skills/resume-writing/SKILL.md` and follow it. Use my notes in `.local/profile.md` to draft an English résumé for a US data-analyst role. Do not invent metrics. Deliver Markdown for my review; I do not have a job posting yet.

For an academic application:

> Read `skills/academic-cv/SKILL.md` and follow it. Use `.local/academic-notes.md` and `.local/fellowship-call.md` to draft my CV. Preserve author order and publication status, follow the call's limits, and keep open questions outside the CV.

Create/provide the private input files named in your request. They are examples of locations, not files shipped with this repository. See [more requests](examples/requests.md) for tailoring, review-only, translation, and ambiguous-CV cases.

### Optional: install in your agent's skills directory

Copy **the entire chosen skill folder**, including `references/`, into a supported skill root. You may install either package independently. Check for an existing same-named destination before copying; do not overwrite local customizations blindly.

| Host | Documented project location | Documented personal location | Explicit use after discovery |
| --- | --- | --- | --- |
| Codex | `.agents/skills/<skill-name>/` | `~/.agents/skills/<skill-name>/` | `$resume-writing` or `$academic-cv` |
| Claude Code | `.claude/skills/<skill-name>/` | `~/.claude/skills/<skill-name>/` | `/resume-writing` or `/academic-cv` |
| Other hosts | Follow the installed host's supported skill contract, or use explicit file reading | Host-dependent | Do not assume slash commands are portable |

Locations and invocation are based on [OpenAI's documentation](https://learn.chatgpt.com/docs/build-skills) and [Claude Code's documentation](https://code.claude.com/docs/en/skills), checked 2026-11-22. Native discovery and invocation have **not** been runtime-tested here. A plain `skills/` source directory is not automatically discovered by every host. No installer, plugin package, or global setup is provided or run.

## How it works

1. **Resolve purpose:** audience, locale, language, request type, and application constraints.
2. **Establish facts:** use candidate-authored notes; separate supported claims, unknowns, and contradictions.
3. **Select evidence:** map a supplied posting/call to real qualifications; retain honest gaps.
4. **Write and review:** improve structure and wording while preserving titles, dates, contribution, and qualifiers.
5. **Verify delivery:** check facts; inspect actual requested exports when tools exist; report missing checks accurately.

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
