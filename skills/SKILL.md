---
name: custom-sow-from-brd
description: Use when the user uploads a BRD and asks for a custom Statement of Work (SOW) built from Airia's Professional Services SOW template — only the Service Overview's use-case list changes, everything else in the template stays fixed.
---

# Custom SOW from BRD

## When to use
Trigger when the user provides a BRD (or equivalent requirements doc) and asks for a
custom Statement of Work, using Airia's Professional Services SOW template as the base.

## The rule that matters most
This template is legal/commercial boilerplate that has already been approved. The ONLY
thing that may change between customers is the numbered use-case list inside Section 3
("Service Overview" → "In-Scope Professional Services"), where the original template has
a single placeholder line: `1. [insert]`.

Everything else — Sections 1, 2, 4, 5, 6, the Phase/Tasks/Activities/Owner table, the
"Services Approach" paragraph, all headings, numbering, and wording — must be reproduced
**exactly**, character for character, from `references/sow_template_reference.md`. Do not
paraphrase, shorten, reorder, or "improve" any of that text. Do not add sections. Do not
remove sections. If asked to change something outside the use-case list, say plainly that
this skill only customizes the Service Overview's use-case list, and ask whether they want
a manual edit made outside the skill's scope instead.

## Process

1. **Read `references/sow_template_reference.md` first.** It is the full, verbatim
   canonical text of the template, with the one customizable block marked
   `[[CUSTOMIZE: USE CASE LIST]]`.

2. **Read the uploaded BRD in full.** Identify the specific AI use case(s) the customer
   wants Airia's Professional Services to help design/build/deploy — this is usually
   stated as the project's objective, the agent(s) to be built, or the business problem
   being solved. Do not use generic language ("AI implementation") if the BRD names a
   specific use case ("customer support ticket triage agent", "invoice data extraction
   agent") — pull the actual use case name/description across verbatim from the BRD's own
   wording where possible.

3. **Replace only `[[CUSTOMIZE: USE CASE LIST]]`** with a numbered list, one line per
   use case, matching the template's original terse style (the original was
   `1. [insert]` — a short phrase, not a paragraph). If the BRD describes multiple
   distinct use cases, list each as its own numbered item. If the BRD is genuinely
   unclear about what the use case is, stop and ask the user rather than guessing or
   inventing one — this field feeds a commercial/legal document.

4. **Leave the Phase/Tasks/Activities/Owner table, "Services Approach," and Sections
   1, 2, 4, 5, and 6 untouched.** These describe Airia's standard delivery methodology
   and legal assumptions, not the specific use case, and do not vary by customer or BRD.

5. **Generate the output as a Word document (.docx)** so the customer receives an
   editable, professional file. Read the `docx` skill before building it, and mirror the
   template's visual structure as closely as the source allows: numbered section
   headings in the same blue accent style, the table with borders, and the Airia
   branding/logo treatment at the top if a template file (not just text) is available.
   If only the text template is available (no source .docx/logo), build a clean
   professional document with the same heading hierarchy and table, and note to the user
   that exact visual fidelity (logo, exact fonts) depends on having the original .docx —
   offer to match it precisely if they can supply that file.

6. **Before delivering, diff your output against `references/sow_template_reference.md`**
   section by section (excluding the customized use-case list) to confirm nothing else
   drifted — no reworded sentences, no dropped clauses, no renumbered sections.
