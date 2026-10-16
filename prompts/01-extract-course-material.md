# SY0-701 Course Material Extraction Pipeline

## Goal

Build a complete, source-grounded Markdown knowledge base from the
CompTIA Security+ SY0-701 bootcamp slide PDFs.

Extract all relevant slide content into objective-specific notes,
validate each note against the original slides, assess coverage
against the official CompTIA exam objectives, and maintain accurate
progress records.

Work through the objectives in exam-weight order:
Domain 4 → Domain 2 → Domain 5 → Domain 3 → Domain 1.

Process one sub-objective at a time. Complete extraction, validation,
coverage assessment, and tracking updates before moving to the next
objective, unless compute or context limits require stopping.

## 1. Read project instructions first

- Read CLAUDE.md, AGENTS.md, and relevant repository documentation.
- Inspect the existing notes, objective_mapping.md, coverage_tracker.md,
  glossary, study log, and available source files.
- Reuse the existing note format and repository conventions.
- Never read or cite files outside the repository, including the
  duplicate /home/joshua/Documents/SecPlus/Slides/ directory.
- Do not install system packages. Existing tools include pdftoppm,
  pdfinfo, and tesseract.

## 2. Establish the current state

Before doing work:
- Read the Resume state section in coverage_tracker.md.
- Identify the first incomplete objective in the required queue.
- Inspect its page-level progress and existing note.
- Verify the source range against the section roadmap and divider
  slides. Page boundaries are provisional until visually confirmed.
- Do not redo pages already fully reviewed and recorded.
- Do not overwrite existing validated notes without a clear reason.

The tracker is the source of truth for page-level progress.
objective_mapping.md is the source of truth for objective-level
coverage status.

## 3. Extract the complete objective

For each objective:

1. Render the relevant PDF pages into .render_cache/ (gitignored).
2. Read every page image using vision. OCR text is a cross-check only;
   OCR alone is not sufficient for extraction.
3. Capture all relevant content, including:
   - Definitions and terminology
   - Procedures and ordered steps
   - Tables and comparisons
   - Diagrams, flows, and relationships
   - Commands, configuration, and CLI output
   - Acronyms, examples, exceptions, and instructor-specific details
   - Warnings, distinctions, and potentially incorrect slide content
4. Preserve the meaning and terminology of the source. Do not silently
   correct slide errors or replace source wording with outside knowledge.
5. Mark unreadable, conflicting, or missing material as [ILLEGIBLE],
   [CONFLICT], or [GAP]. Never invent missing content.
6. Write the extracted material to the correct
   course-unit-notes/<domain-folder>/<objective-slug>.md file.

Match the structure of the existing validated 4.8 note, including
front matter, source information, extraction/validation status, and
source citations.

Every substantive claim must cite its exact slide page:
(Source: PtN p.X)

Cite multiple pages only when a claim genuinely spans them. Place
citations beside the content they support, including relevant table
rows and diagram descriptions.

## 4. Validate against the original slides

Extraction and validation are separate phases of the same objective
workflow. Do not finish extraction and then defer validation while
moving on to another objective.

After extraction:
- Reopen and visually compare every page against the note.
- Check for omissions, transcription errors, incorrect values,
  unsupported claims, missing table entries, and inaccurate citations.
- Correct the note and recheck any changed material.
- Record the validation scope, pages checked, and corrections made.
- Do not treat grep or automated checks as substitutes for visual
  comparison.

Mark the note Validated only after the full source range has passed
validation.

## 5. Assess official objective coverage

Compare the validated note with every official sub-bullet for the
objective in objective_mapping.md or the official CompTIA objective
list already included in the repository.

At the end of each note, include an Official-objective gap check.
For each official sub-bullet, record:
- Covered: adequately explained in the slides and represented in
  the note, with a supporting page citation.
- Weak: mentioned but insufficiently explained, or only partially
  addressed.
- Not in slides: absent from the reviewed source material.

Record specific gaps in both the note and the Gaps column in
objective_mapping.md. Do not silently fill gaps with outside knowledge.
Any optional supplemental research must be clearly labeled
[OUTSIDE-SLIDES] and excluded from source-validation claims.

Use statuses consistently:
- Not Assessed: coverage has not yet been evaluated.
- Unverified: extraction or validation is incomplete.
- Weakly Covered: validated source material leaves meaningful gaps.
- Well Covered: the note is validated and adequately addresses the
  official objective bullets.

A faithful, validated note can still be Weakly Covered.
Never mark an objective Well Covered just because its slides were
completely extracted.

## 6. Update repository records

Once the objective has been fully extracted, validated, and assessed:

- coverage_tracker.md:
  Update page-level Visual_Reviewed, Note_Extracted, Validated,
  and Notes_File fields. Verify expected versus completed page counts.
- objective_mapping.md:
  Update status, source pages, confidence, review date, and specific
  coverage gaps.
- glossary/README.md:
  Add relevant terms with links to their notes. Avoid duplicate entries.
- user_progress/study_log.md:
  Append a session entry listing completed work and the remaining queue.
  Never rewrite or delete prior study-log entries.
- coverage_tracker.md:
  Update the Resume state section with completed work, the current
  objective, the next task, and remaining ranges.

Do not use .render_cache/build_tracker.py if it would overwrite
manually maintained progress flags. Inspect its behavior first.

## 7. Save progress and recover safely

Save work incrementally, approximately every five pages and before
stopping.

For an objective in progress, record:
- Pages completed
- Pages remaining
- Next page to process
- Extraction status
- Validation status

Write partial notes to disk as work proceeds. Clearly label them
In Progress and never claim that a partial note is complete.

If compute, context, or time is running low:
1. Stop starting new work.
2. Save the current note and all progress records.
3. Record the exact next page and next action.
4. Leave the objective incomplete if validation or coverage assessment
   remains unfinished.
5. Resume that objective next session before moving to the next one.

Do not sacrifice validation to maximize the number of objectives
processed.

## 8. Completion checks

Before declaring an objective complete, verify:
- Every page in the confirmed range was visually reviewed.
- Every relevant slide detail is represented in the note.
- Every substantive claim has a supporting source citation.
- The complete note passed visual validation.
- Every official objective bullet has a documented coverage result.
- Gaps and statuses agree across the note and objective mapping.
- Page-level tracker counts match the actual work completed.
- The glossary and append-only study log are updated.
- The Resume state points to the correct next task.

Before ending a session, inspect git status. Do not commit unless
explicitly asked.

## 9. Session report

Report concisely:
- Objectives extracted, validated, and assessed
- Page ranges and counts completed
- Coverage gaps or source errors discovered
- Files changed
- Any incomplete objective and its exact resume point
- The next objective in the queue

After each fully validated objective, offer a practice batch of no
more than 10–15 questions. Do not bulk-generate questions.

Continue in exam-weight order until the work is complete or resources
require a safe stop. Never ask whether to validate an objective:
validation is mandatory before proceeding.
