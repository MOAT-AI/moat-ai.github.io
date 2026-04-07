# MOAT Homepage Content Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Replace the placeholder MOAT homepage copy with a coherent first-pass public narrative grounded in the approved design spec and the `Vision` source material.

**Architecture:** The work stays within the existing Jekyll homepage structure. We will update the hero content in `index.md`, then rewrite each markdown-backed homepage section in `_sections/` so the site reads as one narrative with a clear distinction between current facts and planned ecosystem elements.

**Tech Stack:** Jekyll, Markdown, YAML front matter, existing home layout in `_layouts/home.html`

---

## File Map

- Modify: `index.md`
  - Replace scaffolded hero copy with publication-ready MOAT overview text.
- Modify: `_sections/01-introduction.md`
  - Rewrite placeholder introduction and vision content.
- Modify: `_sections/02-participants.md`
  - Replace placeholder participant scaffolding with verified first-pass collaboration description.
- Modify: `_sections/03-get-involved.md`
  - Replace placeholder participation notes with careful public-facing engagement language.
- Modify: `_sections/04-ai-enabled-ecosystem.md`
  - Replace placeholder ecosystem scaffolding with emerging capability description.
- Reference: `Vision/Starting_point/The MOAT Collaboration.md`
  - Source language for core facts and ecosystem themes.
- Reference: `docs/superpowers/specs/2026-04-07-moat-homepage-content-design.md`
  - Approved content design and editorial boundaries.

### Task 1: Rewrite the homepage hero

**Files:**
- Modify: `index.md`
- Reference: `Vision/Starting_point/The MOAT Collaboration.md`
- Reference: `docs/superpowers/specs/2026-04-07-moat-homepage-content-design.md`

- [ ] **Step 1: Review the current hero fields and source language**

Read:

```md
hero_title: Multi-Office Accelerator Team (MOAT) Collaboration
hero_tagline: A shared space for vision, participation, and AI-enabled collaboration across offices and partners.
hero_note: This homepage is scaffolded from markdown content using Jekyll. Replace placeholder text and image callouts with approved MOAT materials as they become available.
```

Source facts to preserve:

```md
The Multi Office particle Accelerator Team (MOAT) collaboration was created in 2025 as part of the US DOE Genesis Mission (GM).
```

- [ ] **Step 2: Replace the hero with publication-ready copy**

Update `index.md` front matter to:

```md
---
title: MOAT Collaboration
layout: home
hero_title: Multi-Office Accelerator Team (MOAT) Collaboration
hero_tagline: A cross-institutional collaboration advancing AI-assisted tools, shared infrastructure, and coordinated innovation for particle accelerators.
hero_note: Created in 2025 as part of the U.S. Department of Energy Genesis Mission, MOAT brings together laboratories and partners to coordinate AI-related activities for particle accelerators and build a shared technical ecosystem.
---
```

- [ ] **Step 3: Review the updated hero for tone and consistency**

Check that:

- `hero_tagline` is public-facing and readable.
- `hero_note` names the Genesis Mission and MOAT purpose without sounding like internal scaffolding.
- The text does not imply funding outcomes or operational maturity beyond the approved spec.

- [ ] **Step 4: Verify the file diff is limited to hero content**

Run: `git diff -- index.md`

Expected:

- Only front matter text changes appear.
- No layout or formatting regressions are introduced.

- [ ] **Step 5: Commit the hero rewrite**

```bash
git add index.md
git commit -m "Rewrite MOAT homepage hero copy"
```

### Task 2: Rewrite the introduction section

**Files:**
- Modify: `_sections/01-introduction.md`
- Reference: `Vision/Starting_point/The MOAT Collaboration.md`
- Reference: `docs/superpowers/specs/2026-04-07-moat-homepage-content-design.md`

- [ ] **Step 1: Review the current introduction placeholder**

Current placeholder content to replace:

```md
## What Is MOAT?

The **Multi-Office Accelerator Team (MOAT) Collaboration** is a placeholder description for a cross-office effort focused on coordination, shared priorities, and sustained collaboration.
```

- [ ] **Step 2: Rewrite the introduction body**

Replace the body content under the existing front matter with:

```md
## What Is MOAT?

The **Multi-Office Accelerator Team (MOAT) Collaboration** was created in 2025 as part of the U.S. Department of Energy Genesis Mission. It began as a seed effort within the Genesis Mission's Transformational AI Model Consortium, bringing together seven national laboratories to coordinate AI-related activities for particle accelerators.

MOAT provides a shared framework for connecting institutions, technical efforts, and emerging tools across the accelerator community. The collaboration is intended to support coordination, reuse, and joint progress in areas where AI can strengthen accelerator science, engineering, and operations.

## Vision

MOAT is building toward a durable collaboration model that links laboratories, researchers, software efforts, and future partners around common goals for AI-assisted accelerator work. In the near term, the collaboration aims to align proposals, technical priorities, and shared capabilities. Over time, it can help lower barriers to collaboration and create a stronger national ecosystem for AI-enabled particle accelerator research and development.
```

- [ ] **Step 3: Review the introduction against the approved boundaries**

Check that:

- The section clearly distinguishes MOAT's origin from its longer-term vision.
- The wording does not invent governance details.
- The language stays formal but approachable.

- [ ] **Step 4: Verify the section renders as a clean narrative**

Run: `git diff -- _sections/01-introduction.md`

Expected:

- Placeholder bullets are removed.
- The section reads as two short prose blocks with clear headings.

- [ ] **Step 5: Commit the introduction rewrite**

```bash
git add _sections/01-introduction.md
git commit -m "Draft MOAT introduction section"
```

### Task 3: Rewrite the participants section

**Files:**
- Modify: `_sections/02-participants.md`
- Reference: `Vision/Starting_point/The MOAT Collaboration.md`
- Reference: `docs/superpowers/specs/2026-04-07-moat-homepage-content-design.md`

- [ ] **Step 1: Review the verified participant facts**

Verified source material:

```md
... involving seven national laboratories (LBNL, ANL, BNL, FNAL, JLAB, ORNL, SLAC), the MOAT collaboration is growing, with additional participants from national labs, academia and industry.
```

- [ ] **Step 2: Replace the participant placeholder content**

Replace the body content under the existing front matter with:

```md
## Current Collaboration Footprint

MOAT began with participation from seven national laboratories:

- Lawrence Berkeley National Laboratory (LBNL)
- Argonne National Laboratory (ANL)
- Brookhaven National Laboratory (BNL)
- Fermi National Accelerator Laboratory (FNAL)
- Thomas Jefferson National Accelerator Facility (JLAB)
- Oak Ridge National Laboratory (ORNL)
- SLAC National Accelerator Laboratory (SLAC)

This initial group provides the foundation for coordination across accelerator-focused AI activities within the Genesis Mission context. The collaboration is also intended to grow over time through additional participation from other national laboratories, academia, and industry.
```

- [ ] **Step 3: Review for accuracy and restraint**

Check that:

- Only verified laboratories are named.
- The section does not imply a complete or final membership roster.
- No unverified roles, offices, or contacts are introduced.

- [ ] **Step 4: Verify the participant list is readable in markdown**

Run: `git diff -- _sections/02-participants.md`

Expected:

- The placeholder table and prompts are gone.
- The lab list is rendered as a simple bullet list followed by one short explanatory paragraph.

- [ ] **Step 5: Commit the participants rewrite**

```bash
git add _sections/02-participants.md
git commit -m "Draft MOAT participants section"
```

### Task 4: Rewrite the get involved section

**Files:**
- Modify: `_sections/03-get-involved.md`
- Reference: `Vision/Starting_point/The MOAT Collaboration.md`
- Reference: `docs/superpowers/specs/2026-04-07-moat-homepage-content-design.md`

- [ ] **Step 1: Review the participation constraint**

Verified source material:

```md
The participation to MOAT is voluntary. Participants can choose to join, leave or rejoin the collaboration at any time.
```

- [ ] **Step 2: Replace the placeholder participation guidance**

Replace the body content under the existing front matter with:

```md
## Ways To Participate

Participation in the MOAT collaboration is voluntary. The collaboration is intended to provide an open coordination space for organizations and contributors who want to help shape AI-related activities for particle accelerators.

Potential participants may engage by contributing technical ideas, joining collaborative discussions, helping develop shared tools and workflows, or aligning proposal and demonstration efforts with the broader MOAT vision. As the collaboration matures, additional participation pathways and public contact points can be added here.
```

- [ ] **Step 3: Review the section for honesty and tone**

Check that:

- The section feels welcoming without inventing live onboarding resources.
- The final sentence clearly marks future participation details as not yet published.
- The prose is brief enough for a homepage section.

- [ ] **Step 4: Verify there are no fake calls to action**

Run: `git diff -- _sections/03-get-involved.md`

Expected:

- Placeholder links and bullets are removed.
- No email addresses, forms, calendars, or guides are introduced.

- [ ] **Step 5: Commit the get involved rewrite**

```bash
git add _sections/03-get-involved.md
git commit -m "Draft MOAT participation section"
```

### Task 5: Rewrite the AI-enabled ecosystem section

**Files:**
- Modify: `_sections/04-ai-enabled-ecosystem.md`
- Reference: `Vision/Starting_point/The MOAT Collaboration.md`
- Reference: `docs/superpowers/specs/2026-04-07-moat-homepage-content-design.md`

- [ ] **Step 1: Review the ecosystem source list**

Source ecosystem themes:

```md
* Osprey agentic platform
* Virtual Accelerators & Digital Twins factory
* "Marketplaces" w/ benchmarks
 * LLMs
 * skills
 * Workflows
 * Codes
 * ?
* Shared toolset with standardized language and interfaces
```

- [ ] **Step 2: Replace the placeholder ecosystem section**

Replace the body content under the existing front matter with:

```md
## Scope

The MOAT collaboration is helping shape an AI-enabled ecosystem for particle accelerators that supports shared experimentation, reusable tools, and stronger coordination across institutions. This ecosystem is emerging alongside the collaboration itself and is intended to make it easier to develop, compare, and apply AI-assisted approaches across accelerator use cases.

## Core Elements

- **Agentic platforms:** including efforts such as Osprey that can support more capable scientific and technical workflows.
- **Virtual accelerators and digital twins:** shared environments for modeling, testing, and demonstration.
- **Marketplaces and benchmarks:** common spaces for comparing models, skills, workflows, codes, and related assets.
- **Shared interfaces and tooling:** a more standardized language for connecting tools, teams, and technical components across the ecosystem.

These elements describe the collaboration's technical direction rather than a fully finished product stack. As MOAT evolves, this section can expand to highlight concrete repositories, services, benchmarks, and demonstrations.
```

- [ ] **Step 3: Review for ambition versus precision**

Check that:

- The section sounds forward-looking but not inflated.
- Osprey, virtual accelerators, benchmarks, and shared tooling are all represented.
- The closing sentence clearly marks the ecosystem as emerging.

- [ ] **Step 4: Verify the markdown structure is concise**

Run: `git diff -- _sections/04-ai-enabled-ecosystem.md`

Expected:

- Placeholder headings are replaced with one introductory paragraph, one bulleted list, and one closing paragraph.
- The section remains scannable on the homepage.

- [ ] **Step 5: Commit the ecosystem rewrite**

```bash
git add _sections/04-ai-enabled-ecosystem.md
git commit -m "Draft MOAT ecosystem section"
```

### Task 6: Run whole-page consistency review

**Files:**
- Modify if needed: `index.md`
- Modify if needed: `_sections/01-introduction.md`
- Modify if needed: `_sections/02-participants.md`
- Modify if needed: `_sections/03-get-involved.md`
- Modify if needed: `_sections/04-ai-enabled-ecosystem.md`
- Reference: `docs/superpowers/specs/2026-04-07-moat-homepage-content-design.md`

- [ ] **Step 1: Read the final homepage content as one narrative**

Review these files in order:

```text
index.md
_sections/01-introduction.md
_sections/02-participants.md
_sections/03-get-involved.md
_sections/04-ai-enabled-ecosystem.md
```

Check for:

- repeated phrases such as "AI-related activities for particle accelerators"
- inconsistent naming of MOAT or the Genesis Mission
- mismatches between current facts and future-facing language

- [ ] **Step 2: Make small editorial fixes if needed**

Allowed changes:

- tighten repeated wording
- align tense across sections
- shorten any paragraph that feels too dense for a homepage

Do not add:

- new facts not present in the source material
- new contact mechanisms
- new structural sections

- [ ] **Step 3: Verify the full content diff**

Run: `git diff -- index.md _sections/01-introduction.md _sections/02-participants.md _sections/03-get-involved.md _sections/04-ai-enabled-ecosystem.md`

Expected:

- Only content copy changes appear.
- All placeholder language is removed from body text.
- The site now reads like a coherent first-pass public homepage.

- [ ] **Step 4: Optionally build locally if the user requests it**

Run only if asked:

```bash
bundle exec jekyll build
```

Expected:

- Successful static site build with the updated markdown content.

- [ ] **Step 5: Commit the final editorial pass**

```bash
git add index.md _sections/01-introduction.md _sections/02-participants.md _sections/03-get-involved.md _sections/04-ai-enabled-ecosystem.md
git commit -m "Replace MOAT homepage placeholder content"
```
