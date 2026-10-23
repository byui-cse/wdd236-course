---
title: Competency Guide
description: The WDD 236 competencies (six required and one optional), each divided into assessable slices you can choose from when writing a weekly learning contract.
time: 20 minutes
aiUsage: green
---

## How to use this guide

WDD 236 is competency based. You show what you can do by passing off competencies, and you do that in manageable pieces called **slices**.

- A **competency** is a broad professional skill (for example, accessibility engineering).
- A **slice** is one observable part of that competency. A slice is small enough to practice and demonstrate in about a week.
- Each week, your [learning contract](../../ponder/learning-contract/) names the slices you will work on.
- A competency is passed off when **every slice in it** has been demonstrated at Proficient or better.

Slice IDs (for example `3.2`) are used in contracts, peer reviews, and pass-offs. Always cite the ID and name.

### Proficiency levels

| Level          | What it means                                                                                                                                                  |
| -------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Not yet**    | The work does not run, cannot be explained, or the student cannot adapt it when a small variation is introduced.                                               |
| **Proficient** | The work meets the slice's evidence, and you can explain your decisions and handle a small variation live. Required to pass.                                   |
| **Advanced**   | Proficient, plus you chose a harder case, justified tradeoffs against alternatives, found and fixed a non-obvious problem, or could teach the slice to a peer. |

### Evidence every slice needs

Whatever slice you choose, bring:

1. A working artifact (code, document, or report).
2. A short explanation of the important decisions.
3. A verification (test, audit, or experiment) that you ran yourself.
4. One problem, limitation, or tradeoff you discovered.

The "Evidence" column below describes the specific artifact for each slice.

### Cross-cutting practices

Two practices are not competencies of their own, but they appear in every contract:

- **Debugging and evidence-based troubleshooting:** form a hypothesis, test it, and record what you learned.
- **Responsible AI use:** most of your code will be AI-generated, so record your prompts, how you verified the output, and what you overrode. Competency 6 assesses this directly using the evidence you collect in every contract.

### Live check-ins

Each pass-off includes a short live check-in (about five minutes) where the instructor or TA introduces a small variation. Typical challenges are listed with each competency. Prepare by predicting how your work will respond and practicing the change yourself.

---

## 1. Frontend Information Architecture & Architectural Blueprinting

**Outcome:** Translate user needs into technical blueprints using sitemaps, wireframes, and design system documentation.

| ID  | Slice                             | I can...                                                                                                | Evidence                                                             |
| --- | --------------------------------- | ------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------- |
| 1.1 | Requirements analysis             | Turn raw user needs into user stories, journeys, and prioritized requirements.                          | A requirements list with at least one journey per user type.         |
| 1.2 | Sitemap and routing               | Produce a sitemap that covers every journey, including error and empty-state routes, with no dead ends. | A sitemap diagram or schema, with each journey traced through it.    |
| 1.3 | Wireframes and interaction states | Wireframe layouts that show data inputs and dynamic states (default, loading, empty, error, disabled).  | Wireframes in a design tool (for example Figma) with states labeled. |
| 1.4 | Design tokens                     | Define color, typography, and spacing tokens and document how they are used.                            | A token document and matching CSS custom properties.                 |
| 1.5 | Component inventory               | Break a design into a modular component map with responsibilities, inputs, and events.                  | A component specification in Markdown.                               |
| 1.6 | Change impact analysis            | Use the blueprint to explain how a requirement change affects components, data, and layout.             | A short written or live walkthrough of a feature pivot.              |

**Live check-in examples:** a feature pivot (filter by date and category) or a constraint collapse (low-end mobile devices in bright sunlight).

---

## 2. Component Engineering & Modular Architecture

**Outcome:** Architect and implement modular JavaScript applications built from reusable, browser-native components.

| ID  | Slice                              | I can...                                                                                                            | Evidence                                                               |
| --- | ---------------------------------- | ------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| 2.1 | Custom elements                    | Define a custom element with lifecycle callbacks and a clear public interface (attributes, properties, and events). | A working custom element with its interface documented.                |
| 2.2 | Templates and slots                | Compose component markup with `<template>` and `<slot>`.                                                            | A component that accepts content through slots.                        |
| 2.3 | Shadow DOM and style encapsulation | Use Shadow DOM so styles do not leak in or out, and prove it in DevTools.                                           | DevTools evidence of isolation, plus an explanation.                   |
| 2.4 | ES modules                         | Organize code with `import` and `export` and without global scope pollution.                                        | A project split into modules with clear boundaries.                    |
| 2.5 | Separation of concerns             | Keep data logic and API configuration out of UI components.                                                         | A refactor of a monolith, with a before-and-after explanation.         |
| 2.6 | Multi-view composition             | Combine components into a multi-view interface with an app shell.                                                   | A running application that composes several components.                |
| 2.7 | Project tooling and build          | Use a package manager, project scripts, a dev server, and a production build, and explain what each does.           | A repository that installs, runs, and builds from documented commands. |

**Live check-in examples:** the style leak (fix with Shadow DOM) or the monolithic split (extract helpers into a module).

---

## 3. Automated Test Engineering

**Outcome:** Apply automated unit and integration testing to ensure application logic is bug-resistant.

| ID  | Slice                          | I can...                                                                                                 | Evidence                                                           |
| --- | ------------------------------ | -------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------ |
| 3.1 | Test tooling                   | Install, configure, and run a test runner (for example Vitest) locally.                                  | A passing run from a documented command.                           |
| 3.2 | Unit tests for logic           | Test data transformations and utilities, including boundaries and bad input, and read a coverage report. | Unit tests with edge cases, and a coverage report you can explain. |
| 3.3 | Strong assertions              | Recognize and fix weak or "false green" tests with strict comparisons.                                   | A weak test that was rewritten, with an explanation.               |
| 3.4 | Component state tests          | Assert component state changes programmatically, without manual browser checking.                        | Tests for state transitions such as open, closed, and disabled.    |
| 3.5 | Integration and workflow tests | Verify a complete user journey across components, using mocked data where needed.                        | A passing workflow test.                                           |

**Live check-in examples:** the red-to-green break (fix a failing test) or the false green (strengthen a weak assertion).

---

## 4. Asynchronous Flow & State Management

**Outcome:** Orchestrate asynchronous data and client-side state without leaks, race conditions, or global scope pollution.

| ID  | Slice                            | I can...                                                                         | Evidence                                                    |
| --- | -------------------------------- | -------------------------------------------------------------------------------- | ----------------------------------------------------------- |
| 4.1 | Promises and async/await         | Write and trace asynchronous code and explain the event loop at a working level. | A data module that uses async/await, with a trace.          |
| 4.2 | Fetching and data mapping        | Retrieve JSON from an API, validate the response, and map it to UI-ready data.   | A fetch module and a network inspection screenshot.         |
| 4.3 | Loading, empty, and error states | Represent every phase of a request in the interface.                             | A UI that visibly handles all four states.                  |
| 4.4 | Defensive error handling         | Catch failed requests and network dropouts without breaking the app.             | A demonstration with the network disabled.                  |
| 4.5 | Local state patterns             | Manage state with closures or state objects and update the UI reactively.        | A state module with a documented flow.                      |
| 4.6 | Shared state and data flow       | Share state across components with a clear, one-directional update path.         | A diagram plus working code connecting multiple components. |
| 4.7 | Persistence                      | Save and restore state safely, validating missing or malformed stored data.      | A refresh test with bad stored data.                        |

**Live check-in examples:** the architecture audit (what happens when the network drops on click) or the state tracing game (trace one interaction back to the state store).

---

## 5. Inclusive Craftsmanship & Accessibility (A11y) Compliance

**Outcome:** Build interfaces that meet professional WCAG standards and work with assistive technology.

| ID  | Slice                         | I can...                                                                                                | Evidence                                                                       |
| --- | ----------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| 5.1 | Semantic structure            | Use landmarks, headings, labels, and native controls correctly.                                         | An outline and a landmark audit of a page.                                     |
| 5.2 | Visual accessibility          | Meet contrast, text sizing, reflow, zoom, and touch-target requirements.                                | Contrast checks and zoom or reflow screenshots.                                |
| 5.3 | Keyboard operation            | Operate every feature with the keyboard, with visible focus.                                            | A keyboard-only walkthrough.                                                   |
| 5.4 | Focus management              | Manage focus for modals, view changes, and dynamic content, including traps and skip links.             | A demonstration of focus entering, staying in, and returning from a component. |
| 5.5 | ARIA and dynamic content      | Apply roles, states, and properties that track component state, and announce updates with live regions. | A list of attributes with a DOM trace of their changes.                        |
| 5.6 | Accessibility tree inspection | Read computed roles and names in DevTools and correct problems.                                         | A before-and-after inspection of a component.                                  |
| 5.7 | Automated and manual auditing | Run Lighthouse or Axe, interpret results, and add manual checks to cover what tools miss.               | An audit report with manual notes.                                             |

**Live check-in examples:** the blindfold test (keyboard only) or the accessibility tree audit (computed role and name).

---

## 6. AI Oversight, Code Auditing & Quality Assurance

**Outcome:** Evaluate and refine AI-generated code, tests, and reviews to ensure technical accuracy.

| ID  | Slice                                        | I can...                                                                                                   | Evidence                                                        |
| --- | -------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------- |
| 6.1 | Prompting with constraints                   | Write prompts that specify native web standards, structure, and accessibility requirements.                | A prompt and its result, with the reasoning for the wording.    |
| 6.2 | Detecting hallucinations and framework bleed | Spot nonexistent APIs, framework-specific patterns, and outdated syntax in AI output.                      | An annotated code sample listing each flaw and why it is wrong. |
| 6.3 | Verification and audit trail                 | Check AI output against documentation, tests, and experiments, and record prompts, overrides, and results. | Verification notes covering at least one complete feature.      |
| 6.4 | Auditing AI-generated tests                  | Find false greens, missing edge cases, and meaningless assertions in AI-written tests.                     | A critique and an improved test suite.                          |
| 6.5 | Auditing for quality and risk                | Review code for maintainability, performance, security, and accessibility problems.                        | A written audit with prioritized findings.                      |
| 6.6 | Pull request review                          | Review an AI-generated change with specific approvals or rejections and justifications.                    | A pull request log or review document.                          |

**Live check-in examples:** spot the hallucination (find the flaw in 15 lines of AI code) or the prompt diagnostic (rewrite a failing prompt).

---

## 7. Performance & Deployment (Optional)

**Outcome:** Deliver a production-quality application as part of a team, measuring and improving its quality and performance.

This competency is completed on a team project. It is required for an A unless you earn Advanced on four other competencies (see the course summary).

| ID  | Slice                                  | I can...                                                                                                       | Evidence                                                                   |
| --- | -------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| 7.1 | Team workflow                          | Break work into tasks with a definition of done, use branches and pull requests, and resolve a merge conflict. | An issue board or task list and a pull request history.                    |
| 7.2 | Linting and formatting                 | Configure ESLint (and a formatter) for the team and fix or justify what it reports.                            | A shared lint configuration and a clean run, with one rule you explain.    |
| 7.3 | Automated quality gates                | Run lint, tests, and the build automatically on every pull request.                                            | A CI workflow that fails on a deliberate problem and passes after the fix. |
| 7.4 | Performance measurement                | Measure performance with Lighthouse and DevTools, and identify the largest bottleneck.                         | A baseline report and a written diagnosis.                                 |
| 7.5 | Performance improvement                | Make a targeted improvement (images, loading strategy, bundle size, caching) and show the result.              | Before-and-after measurements with an explained tradeoff.                  |
| 7.6 | Deployment and production verification | Deploy the app, manage environment configuration, and verify behavior outside the local environment.           | A live URL, plus notes on one local-versus-production difference.          |
| 7.7 | Technical documentation                | Document setup, architecture, and decisions so a new teammate can contribute.                                  | A README and at least one decision record.                                 |

**Live check-in examples:** the regression gate (introduce a failing change and show CI catches it) or the slow page (diagnose a heavy page with Lighthouse and propose a fix).

---

## Choosing slices for a contract

- Choose one primary competency and list the exact slice IDs you will work on.
- Two to four slices is a typical week. Combine slices that naturally support each other (for example 4.2, 4.3, and 4.4).
- Slices with dependencies are easier after the slices before them in the same competency, but you may choose any order that your project supports.
- Revisit a slice at a higher level to move from Proficient to Advanced.
- Use the [recommended contract path](../../ponder/recommended-10-contract-path/) if you want a suggested sequence.
