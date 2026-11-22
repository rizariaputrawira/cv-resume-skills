# ATS compatibility and export

## What the evidence supports

An applicant tracking system can ingest documents, parse fields, support search and screening, and apply employer-configured workflows. Parsing, eligibility filtering, matching/ranking, and a recruiter's decision are different operations. Do not describe every ATS as “just a database” or assume every product uses a score.

[Greenhouse documents parsing failures](https://support.greenhouse.io/hc/en-us/articles/200989175-Unsuccessful-resume-parse) from columns, complex tables/headers/footers, contact information in text boxes, graphics, image uploads, unclear sections, and spaced-out letters. Its stated parsing limit is 2.5 MB. These are vendor-specific observations supporting a conservative layout, not proof that every column or table fails in every ATS.

[Greenhouse's upload guidance](https://support.greenhouse.io/hc/en-us/articles/360052218132-Supported-formats-for-resumes-cover-letters-and-other-candidate-uploads) separately lists DOC, DOCX, PDF, RTF, and TXT with uploads up to 100 MB. That is not its parsing limit. Its [auto-reject documentation](https://support.greenhouse.io/hc/en-us/articles/360000653472-Auto-reject) describes employer-configured rejection based on application-question answers, not a universal résumé score.

Use the current application's instructions first. Recheck vendor limits before an application depends on them; file upload acceptance does not prove parsing support or accuracy. No source here establishes a universal rejection percentage, keyword density, ATS score, or file type accepted by every employer.

## Conservative layout defaults

These are project defaults chosen to reduce documented risks:

- Single-column reading order; normal text paragraphs; conventional section names such as Experience, Education, Projects, and Skills.
- Name and contact details in the main document body. Avoid tables used for layout, text boxes, icons as the only labels, photographs, charts, skill bars, letter spacing, and decorative word art.
- Consistent, complete role/employer/date relationships. Preserve actual organization names and titles; do not invent an “Inc.” suffix just because a parser may prefer it.
- Readable common font, approximately 11–12 pt body text, and approximately 0.5–1 inch margins as a starting range. Adjust for the paper size and content; these are not Harvard or ATS-mandated measurements.
- Use actual text, not a scan or screenshot. A hyperlink's visible label should remain meaningful when copied as plain text.

## File selection

1. Follow the employer's required file type, template, page limit, and maximum size. A requested DOCX takes priority over a personal preference for PDF.
2. If multiple formats are allowed, choose an inspectable text-based PDF for layout stability or DOCX when editability or the receiving workflow favors it. Neither is universally superior for parsing. Keep an editable source where useful; do not mandate both exports when only one is requested.
3. Inspect the available tools before choosing an export route. An installed word processor/converter or authorized document skill may be usable; this package itself provides neither. Do not assume a particular LibreOffice wrapper, renderer, or font is present.
4. Export from the reviewed final source into the private output location. Do not overwrite an existing application version without authorization. Do not install dependencies or use a cloud converter implicitly.

## Verify the final artifact, not just its source

| Check | Required observation | What it does not prove |
| --- | --- | --- |
| Factual audit | Compare identity, roles, dates, metrics, qualifiers, and skills to candidate evidence | Independent credential verification |
| Text extraction | Name, contact details, headings, dates, bullets, links, and non-ASCII text survive in sensible order | Any vendor's successful field mapping or ranking |
| Visual inspection | Inspect every rendered page for clipping, overlap, legibility, broken bullets, orphan headings, and unintended blank pages | Correct parsing or hiring suitability |
| File properties | Actual extension/type, requested page count, and applicable size limit | That upload acceptance means successful parsing |
| Application preview | If the candidate authorizes access, inspect the actual portal's populated fields and correct errors with truthful data | Future screening results or other vendors' behavior |

Use an existing text extractor only if present. For example, an available `pdftotext` can inspect a PDF's text and reading order, and an available `pdfinfo` can report page count. Inspect the text rather than treating nonempty output or a successful exit status as sufficient. DOCX extraction must inspect body content in order; simply unzipping XML and seeing words is not a visual review.

A local text check must be reported as a **text-extraction check**, not “ATS tested,” “ATS passed,” or “100% ATS compatible.” Test data can behave differently from real candidate records; never upload synthetic or real data to an ATS without explicit permission.

If binary generation is unavailable, provide the requested content as Markdown/plain text, identify the absent export, and state that visual/page-count and ATS checks are unperformed. Do not present the file request as completed. A successful export followed by a failed check remains a failed check until corrected.

## Screening and keywords

Employer-defined questions can cause automated rejection independently of résumé layout. Missing evidence for a requirement should remain an explicit gap or clarification, not be “fixed” with keywords or a false eligibility answer. Never invent work authorization or disclose sensitive eligibility information that the candidate did not provide.

Use job terminology for genuine experience and provide both an expanded phrase and acronym when it improves clarity. Avoid keyword stuffing, hidden text, fabricated match scores, and promises of bypassing screening. Human readability and faithful evidence remain the objectives.
