# WDD 236 Course Summary

## Course Overview

WDD 236: Frontend Architecture & Engineering is the bridge between web mechanics and professional frontend product engineering.

Students enter this course after learning foundational mechanics in WDD 235 (HTML, CSS, JavaScript, basic DOM work, and deployment). WDD 236 builds on those fundamentals by emphasizing architecture, maintainability, testing discipline, accessibility, and technical communication.

The course is competency based and student directed. There is no fixed sequence of assignments. Each week students write a **learning contract** that names the competency slices they will work on, build and investigate to produce evidence, and then demonstrate that evidence. The course keeps a consistent standard for what counts as mastery while students choose the projects, resources, and order that fit their needs.

## Instructional Approach

The instructor acts as a mentor and coach rather than a lecturer. Scaffolding is intentionally light: the course supplies clear outcomes, a competency guide, example contracts, feedback, and assessment, and students decide how to get there.

The weekly cycle follows the BYU-Idaho learning model:

- **Prepare:** Students choose a focus, review the [competency guide](../src/content/resources/competencies.md), and write a learning contract with a guiding question, a plan, and the evidence they will produce.
- **Teach One Another:** Students review each contract and the resulting work with a peer, trying to break each other's work and giving specific feedback.
- **Ponder/Prove:** Students reflect on what they learned, investigate unexpected results, and demonstrate the work to the instructor or a TA.

Students are expected to move beyond passive reading by building, testing, comparing, and documenting their decisions.

## The Weekly Learning Contract Cycle

1. **Choose a focus.** Select one primary competency and the specific slices to work on this week. Supporting slices from other competencies may be included.
2. **Write the contract.** Describe your starting point, a guiding question, the resources you will use, what you will practice, the challenges you will test, your first milestone, the evidence you will produce, and how you will use and verify AI.
3. **Review with a peer.** Share the contract, predict how your work will behave, and try to break each other's work. Record what you predicted, what you observed, and what you changed.
4. **Build and investigate.** Create a working increment, test it, and document what you discover.
5. **Pass off.** When you are ready, demonstrate the slices to the instructor or TA, explain your decisions, and handle a small variation live. Use the feedback to choose your next contract.

Contracts may be revised as students learn. Students tell the instructor what changed and why. Slices that are not yet passed off roll forward into later contracts.

For students unsure what to do next, the course offers a recommended 10-contract path and a fully worked first contract as models.

## Competency-Based Framework

Students show what they can do through six required competencies and one optional competency. Each is divided into **slices**: observable pieces of the competency that are small enough to practice and assess within a week. The complete list of slices, with evidence for each, is in the competency guide.

1. **Architecture and system planning:** Translate requirements into sitemaps, wireframes, design tokens, and component maps.
2. **Component engineering and modular architecture:** Build maintainable browser-native components and multi-view UI systems with ES modules, with a project build workflow.
3. **Automated test engineering:** Design and implement reliable unit and integration tests for logic, state, edge cases, and workflows.
4. **Asynchronous flow and state management:** Handle asynchronous data and local and shared state without breaking UI reliability.
5. **Accessibility engineering:** Build accessible interaction paths, semantics, and assistive-technology support from the start.
6. **AI oversight, code auditing, and quality assurance:** Direct AI to produce most of the code, then validate its correctness, maintainability, and risk.
7. **Performance and deployment (optional, team project):** Work with a team to enforce quality with linting and automated checks, measure and improve performance, and deploy.

Two cross-cutting practices appear in every contract: debugging with evidence, and responsible AI-assisted development.

### Proficiency levels

- **Not yet:** The work does not meet the slice's evidence, or the student cannot explain or adapt it.
- **Proficient:** The work meets the evidence, the student explains their decisions, and handles a small variation live.
- **Advanced:** Proficient, plus a harder case, a justified tradeoff, a non-obvious problem solved, or the ability to teach the slice.

## Pass-Off Process

Competencies are passed off one slice or group of slices at a time. A pass-off includes:

- A working artifact.
- An explanation of important decisions.
- A verification the student ran themselves (test, audit, or experiment).
- A discussion of one problem, limitation, or tradeoff.
- A short live check-in (about five minutes) where a small variation is introduced. Each competency has example challenges.

Students can re-demonstrate after feedback. Multiple attempts are expected.

## Learning Outcomes

By the end of WDD 236, students should be able to:

1. Translate user needs into technical blueprints using sitemaps, wireframes, and design system documentation.
2. Architect and implement advanced JavaScript patterns, including reusable components, asynchronous flow, and modular architecture.
3. Apply unit and integration testing to validate logic, async behavior, and complete user workflows.
4. Implement accessibility patterns to ensure products meet professional WCAG standards.
5. Evaluate and refine AI-assisted code and test recommendations for correctness, maintainability, and risk.

These outcomes intentionally extend WDD 235 prerequisite mechanics into professional engineering competencies.

## Pedagogical Principles

- **Student agency with a consistent standard:** Students choose their path, but the evidence for proficiency is the same for everyone.
- **Architecture before implementation:** Students articulate structure and intent before writing significant code.
- **Evidence over assumption:** Claims about quality are demonstrated through tests, audits, and measurable criteria.
- **Explain and adapt:** Working code is not enough; students must explain it and adjust it when conditions change.
- **Accessibility is core engineering:** Accessibility is a first-class quality attribute, not post-launch cleanup.
- **Encapsulation and reuse:** Component design reduces duplication and improves maintainability.
- **Reflective engineering:** Students justify decisions, discuss tradeoffs, and revise based on review feedback.
- **AI-assisted accountability:** AI can accelerate review and idea generation, but students remain responsible for correctness.

## Assessment and Grading

Assessment is competency based and mastery focused. Students collect evidence across weekly contracts and can improve demonstrations after feedback.

The course is treated as pass/fail with a grade tier:

- **B:** Pass off all required competencies (every slice) at Proficient or better.
- **A:** In addition, either demonstrate Advanced mastery on four or more competencies or pass off competency 7 (Performance and deployment) at Proficient or better.

Primary evidence includes:

- Architecture artifacts (sitemaps, wireframes, technical plans, component maps)
- Component implementation quality (modularity, clarity, maintainability)
- Automated test depth and reliability
- State and data flow correctness for local and asynchronous scenarios
- Accessibility checks for static and dynamic interfaces
- Learning contracts, peer reviews, and investigation notes
- AI audit trails and code-review records

## AI Use in This Course

AI is a learning support tool, not a replacement for student thinking. In WDD 236, students are expected to use AI to generate most of their code, following the specify, generate, inspect, test, revise, and explain workflow. The student's work is the specification, the review, the verification, and the decisions.

- General tutoring and research use is allowed.
- Assignment-specific limits are communicated with stoplight indicators (green, yellow, red).
- Each contract states how AI will be used and how its output will be verified.
- Students review, verify, and adapt all AI-generated output, and must be able to explain the final work as their own.

In WDD 236, AI use emphasizes high-level engineering review:

- UX and architecture critique during planning
- Test case generation, especially boundary and edge scenarios
- Code smell and maintainability audits
- Accessibility walkthrough simulation and remediation suggestions
- Final quality review against explicit standards

Students validate AI output by tracing reasoning, running tests, and checking documentation.

## Tools and Workflow Expectations

- VS Code (recommended)
- Node.js (LTS)
- Git and GitHub
- A `contracts` folder and a `reviews` folder in the student's work directory for learning contracts and peer reviews
- Team and communication tools as needed

Recommended technical stack elements include:

- Browser-native component APIs
- Modern JavaScript modules and async patterns
- Automated testing frameworks (for example, Vitest)
- Accessibility and lint/audit tooling

## Summary

WDD 236 develops frontend engineers, not just coders. Through weekly learning contracts, students take ownership of their path while the competency slices keep the standard clear: architecture practice, component engineering, automated quality strategies, accessibility, and responsible AI-assisted review, demonstrated with evidence and explained in the student's own words.
