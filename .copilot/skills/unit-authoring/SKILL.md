---
name: unit-authoring
description: Reusable workflow for aligning Prepare, Ponder, and Prove across a unit with a two-week arc, gap mapping, and end-of-unit synthesis requirements.
---

# Unit Authoring Workflow Skill

## Purpose

Use this skill to design or refactor a unit so that Prepare, Ponder, and Prove form one coherent learning sequence.

This skill mirrors the process used to complete Unit 1 in this repository.

## Use When

- A unit's Prove assignment has changed and Prepare/Ponder must be realigned.
- Weekly activities feel disconnected from the final deliverable.
- Students are asked to submit artifacts they were not explicitly taught how to produce.
- You need a repeatable way to build Unit 2+ using the same structure as Unit 1.

## Inputs Required

1. Unit overview file in `src/content/units`.
2. Prepare activities for the unit in `src/content/prepare`.
3. Existing or target Prove assignment in `src/content/prove`.
4. Existing Ponder activities in `src/content/ponder`.

## Core Principle

Every major item required in Prove must be introduced in Prepare and reinforced before final submission.

Ponder can do this in two valid ways:

1. Direct scaffolding: practice that maps directly to a Prove artifact.
2. Supporting skill practice: practice of concepts or techniques students will apply in Prove, even if the Ponder output is not submitted directly.

If Prove includes an artifact not scaffolded earlier, add missing instruction or practice before keeping the requirement.

## Workflow

### Phase 1: Audit and Gap Map

1. Read the unit overview, both weekly Prepare files, linked Ponder items, and the Prove assignment.
2. Extract required Prove artifacts into a checklist.
3. Map where each artifact is first introduced, practiced, and finalized.
4. Identify gaps, duplicates, and timing mismatches.

Deliverable:

- A short gap map: `Artifact -> Prepare intro -> Ponder practice -> Prove completion`.

### Phase 2: Define Two-Week Learning Arc

1. Week 1: problem framing and scope.
2. Week 2: artifact quality and integration.
3. Prove due end of unit: synthesis plus extension.

Suggested Week 1 outputs:

- Problem statement
- MVP boundaries (in/out)
- Persona
- Initial user stories

Suggested Week 2 outputs:

- One selected story + acceptance criteria
- Critical workflow (trigger/path/error/success)
- Sitemap + IA risk
- Wireframes + accessibility annotation

### Phase 3: Update Prepare Activities

For each Prepare file:

1. Ensure terms/topics list covers required concepts before they are submitted.
2. Add or adjust submission bullets to help students show that they have mastered the required concepts.
3. Keep workload realistic for 60-90 minutes.
4. Support freedom for the student to use any resource they prefer but add optional readings or resources to support each required concept.

Rule:

- Do not request an artifact in submission if no reading or guidance introduces it.

### Phase 4: Add/Update Ponder Practice

Create one Ponder activity per week.

Week 1 Ponder should:

1. Reinforce scope decisions.
2. Include lightweight templates/examples.
3. Practice persona/story drafting and boundary decisions, or a supporting skill needed for those decisions.

Week 2 Ponder should:

1. Pressure-test workflow, IA, and wireframes.
2. Add coherence checks (persona -> story -> workflow -> sitemap -> wireframe).
3. Include prompts that catch scope creep, or focused practice on a workflow/UX quality skill used in Prove.

### Phase 5: Upgrade Prove from Draft Collection to Final Proposal

Prove should require students to:

1. Consolidate work from Prepare/Ponder.
2. Revise and polish drafts.
3. Expand to a complete planning package.

Recommended extension requirements:

- Story expansion and prioritization
- Acceptance criteria for key stories
- Sitemap expansion to cover must-have flows
- Additional wireframes for new must-have views
- Explicit coherence mapping across artifacts

### Phase 6: Align Rubric to New Expectations

Rubric criteria should match exactly what students are asked to submit.

At minimum include:

1. Scope and problem clarity
2. Story quality/prioritization
3. Workflow completeness
4. IA coverage and logic
5. Wireframe coverage/annotation/accessibility
6. Reflection and tradeoff quality

### Phase 7: Validate

1. Run `pnpm build`.
2. Fix frontmatter, heading, or route issues.
3. Confirm new internal links resolve.

## Definition of Done

A unit is done when:

1. Prove requirements are fully scaffolded by Prepare and Ponder.
2. Week 1 and Week 2 each have clear purpose and outputs.
3. Prove is explicitly end-of-unit synthesis and extension, not just a copy of drafts.
4. Rubric mirrors assignment requirements.
5. Site builds successfully.

## Reusable Prompt Template

Use this prompt when updating another unit:

"Apply the Unit Authoring Skill to [unit-id].

- Keep the same two-week pattern used in Unit 1.
- Audit Prepare/Ponder/Prove for gaps.
- Ensure each Prove artifact is introduced in Prepare and reinforced through either direct Ponder scaffolding or supporting skill practice.
- Make Prove an end-of-unit synthesis + extension deliverable.
- Add or revise one Ponder per week.
- Update rubric criteria to match requirements.
- Run `pnpm build` and fix content issues."
