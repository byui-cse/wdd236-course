# WDD 236 Competency Progress Tracker

Use this tracker to record evidence for each competency slice. A competency is passed off when every slice in it has been demonstrated at **Proficient** or better. The Performance & Deployment competency is optional, with the course-grade condition described below.

- Add a peer's name and the review date after you explain the slice and discuss their questions.
- Add a link or short note to the working artifact and its verification.
- Bring your evidence and be ready to explain your decisions, a limitation or tradeoff, and respond to a small variation during the live check-in.
- Do not check **Competency passed** until every slice has been demonstrated at Proficient or better and you have completed the instructor/TA pass-off.

Student: ____________________________________  
Project: ____________________________________  
Term: ______________________________________

## 1. Frontend Information Architecture & Architectural Blueprinting

Competency passed: [ ]  Date: ______________  Instructor/TA: ______________________________

| Peer reviewed | Instructor reviewed | Slice | Peer name and date | Evidence note or link |
| --- | --- | --- | --- | --- |
| [ ] | [ ] | **1.1 Requirements analysis:** Turn raw user needs into user stories, journeys, and prioritized requirements. |  |  |
| [ ] | [ ] | **1.2 Sitemap and routing:** Map every journey, including error and empty-state routes, without dead ends. |  |  |
| [ ] | [ ] | **1.3 Wireframes and interaction states:** Wireframe layouts and label default, loading, empty, error, and disabled states. |  |  |
| [ ] | [ ] | **1.4 Design tokens:** Define color, typography, and spacing tokens and document their use. |  |  |
| [ ] | [ ] | **1.5 Component inventory:** Specify modular components, responsibilities, inputs, and events. |  |  |
| [ ] | [ ] | **1.6 Change impact analysis:** Explain how a requirement change affects components, data, and layout. |  |  |

## 2. Component Engineering & Modular Architecture

Competency passed: [ ]  Date: ______________  Instructor/TA: ______________________________

| Peer reviewed | Instructor reviewed | Slice | Peer name and date | Evidence note or link |
| --- | --- | --- | --- | --- |
| [ ] | [ ] | **2.1 Custom elements:** Define a custom element with lifecycle callbacks and a documented public interface. |  |  |
| [ ] | [ ] | **2.2 Templates and slots:** Compose component markup with `<template>` and `<slot>`. |  |  |
| [ ] | [ ] | **2.3 Shadow DOM and style encapsulation:** Isolate styles with Shadow DOM and verify the isolation in DevTools. |  |  |
| [ ] | [ ] | **2.4 ES modules:** Organize code with imports and exports, avoiding global scope pollution. |  |  |
| [ ] | [ ] | **2.5 Separation of concerns:** Keep data logic and API configuration out of UI components. |  |  |
| [ ] | [ ] | **2.6 Multi-view composition:** Compose several components into a multi-view interface with an app shell. |  |  |
| [ ] | [ ] | **2.7 Project tooling and build:** Use and explain the package manager, project scripts, dev server, and production build. |  |  |

## 3. Automated Test Engineering

Competency passed: [ ]  Date: ______________  Instructor/TA: ______________________________

| Peer reviewed | Instructor reviewed | Slice | Peer name and date | Evidence note or link |
| --- | --- | --- | --- | --- |
| [ ] | [ ] | **3.1 Test tooling:** Install, configure, and run a test runner locally. |  |  |
| [ ] | [ ] | **3.2 Unit tests for logic:** Test transformations and utilities, including boundaries and bad input; explain a coverage report. |  |  |
| [ ] | [ ] | **3.3 Strong assertions:** Recognize and fix weak or false-green tests with strict comparisons. |  |  |
| [ ] | [ ] | **3.4 Component state tests:** Programmatically test component state transitions such as open, closed, and disabled. |  |  |
| [ ] | [ ] | **3.5 Integration and workflow tests:** Test a complete user journey across components, using mocked data when needed. |  |  |

## 4. Asynchronous Flow & State Management

Competency passed: [ ]  Date: ______________  Instructor/TA: ______________________________

| Peer reviewed | Instructor reviewed | Slice | Peer name and date | Evidence note or link |
| --- | --- | --- | --- | --- |
| [ ] | [ ] | **4.1 Promises and async/await:** Write and trace asynchronous code and explain the event loop at a working level. |  |  |
| [ ] | [ ] | **4.2 Fetching and data mapping:** Retrieve API JSON, validate the response, and map it to UI-ready data. |  |  |
| [ ] | [ ] | **4.3 Loading, empty, and error states:** Represent every phase of a request in the interface. |  |  |
| [ ] | [ ] | **4.4 Defensive error handling:** Handle failed requests and network dropouts without breaking the app. |  |  |
| [ ] | [ ] | **4.5 Local state patterns:** Manage state with closures or state objects and update the UI reactively. |  |  |
| [ ] | [ ] | **4.6 Shared state and data flow:** Share state across components with a clear, one-directional update path. |  |  |
| [ ] | [ ] | **4.7 Persistence:** Save and restore state safely, validating missing or malformed stored data. |  |  |

## 5. Inclusive Craftsmanship & Accessibility (A11y) Compliance

Competency passed: [ ]  Date: ______________  Instructor/TA: ______________________________

| Peer reviewed | Instructor reviewed | Slice | Peer name and date | Evidence note or link |
| --- | --- | --- | --- | --- |
| [ ] | [ ] | **5.1 Semantic structure:** Use landmarks, headings, labels, and native controls correctly. |  |  |
| [ ] | [ ] | **5.2 Visual accessibility:** Meet contrast, text sizing, reflow, zoom, and touch-target requirements. |  |  |
| [ ] | [ ] | **5.3 Keyboard operation:** Operate every feature with the keyboard and visible focus. |  |  |
| [ ] | [ ] | **5.4 Focus management:** Manage focus for modals, view changes, and dynamic content, including traps and skip links. |  |  |
| [ ] | [ ] | **5.5 ARIA and dynamic content:** Keep ARIA roles, states, and properties synchronized and announce updates with live regions. |  |  |
| [ ] | [ ] | **5.6 Accessibility tree inspection:** Inspect computed roles and names in DevTools and correct problems. |  |  |
| [ ] | [ ] | **5.7 Automated and manual auditing:** Run Lighthouse or Axe, interpret results, and add manual checks. |  |  |

## 6. AI Oversight, Code Auditing & Quality Assurance

Competency passed: [ ]  Date: ______________  Instructor/TA: ______________________________

| Peer reviewed | Instructor reviewed | Slice | Peer name and date | Evidence note or link |
| --- | --- | --- | --- | --- |
| [ ] | [ ] | **6.1 Prompting with constraints:** Specify native web standards, structure, and accessibility requirements in prompts. |  |  |
| [ ] | [ ] | **6.2 Detecting hallucinations and framework bleed:** Identify nonexistent APIs, framework-specific patterns, and outdated syntax in AI output. |  |  |
| [ ] | [ ] | **6.3 Verification and audit trail:** Check AI output against documentation, tests, and experiments; record prompts, overrides, and results. |  |  |
| [ ] | [ ] | **6.4 Auditing AI-generated tests:** Find false greens, missing edge cases, and meaningless assertions; improve the tests. |  |  |
| [ ] | [ ] | **6.5 Auditing for quality and risk:** Review code for maintainability, performance, security, and accessibility problems. |  |  |
| [ ] | [ ] | **6.6 Pull request review:** Review an AI-generated change with specific approvals or rejections and justifications. |  |  |

## 7. Optional: Performance & Deployment

This competency is completed on a team project. It is required for an A unless you earn Advanced on four other competencies; see the course summary for details.

Competency passed: [ ]  Date: ______________  Instructor/TA: ______________________________

| Peer reviewed | Instructor reviewed | Slice | Peer name and date | Evidence note or link |
| --- | --- | --- | --- | --- |
| [ ] | [ ] | **7.1 Team workflow:** Break work into tasks with a definition of done, use branches and pull requests, and resolve a merge conflict. |  |  |
| [ ] | [ ] | **7.2 Linting and formatting:** Configure ESLint and a formatter for the team, then fix or justify reported issues. |  |  |
| [ ] | [ ] | **7.3 Automated quality gates:** Run lint, tests, and the build automatically on every pull request. |  |  |
| [ ] | [ ] | **7.4 Performance measurement:** Measure with Lighthouse and DevTools and identify the largest bottleneck. |  |  |
| [ ] | [ ] | **7.5 Performance improvement:** Make a targeted improvement and explain the before-and-after measurements and tradeoff. |  |  |
| [ ] | [ ] | **7.6 Deployment and production verification:** Deploy the app, manage environment configuration, and verify production behavior. |  |  |
| [ ] | [ ] | **7.7 Technical documentation:** Document setup, architecture, and decisions so a new teammate can contribute. |  |  |

## Cross-cutting practice: Debugging and evidence-based troubleshooting

These practices should appear throughout your contracts and pass-offs. They are not a separate competency.

| Practiced | Evidence note or link |
| --- | --- |
| [ ] Form a hypothesis, test it, and record what you learned. |  |
| [ ] Run and record a verification, such as a test, audit, or experiment. |  |
| [ ] Identify a problem, limitation, or tradeoff in your work. |  |

## Cross-cutting practice: Responsible AI use

Record your prompts, how you verified AI output, and what you overrode. Competency 6 assesses this directly using the evidence collected in your contracts.

| Practiced | Evidence note or link |
| --- | --- |
| [ ] Record relevant prompts and the AI-generated output you evaluated. |  |
| [ ] Verify suggestions against documentation, tests, or experiments. |  |
| [ ] Record what you overrode and explain your decisions. |  |

## Next steps

Competency or slice to work on next: _________________________________________________

Why this is the next useful step: ___________________________________________________

Support or resources I will use: ____________________________________________________
