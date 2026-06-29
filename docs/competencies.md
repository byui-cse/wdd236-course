# WDD 236: Competency & Assessment Framework

This document compiles the 6 core competencies for **WDD 236: Professional Frontend Architecture & Engineering** structured for a Competency-Based Education (CBE) model. Each competency is mapped to its specific course outcome and contains a measurable description, mastery criteria, required evidence, and two distinct 5-minute live check-in challenges (Set A and Set B).

---

## 1. Frontend Information Architecture & Architectural Blueprinting

- **Aligned Course Outcome:** Translate user needs into technical blueprints using sitemaps, wireframes, and design system documentation.
- **Measurable Description:** The student can synthesize a set of raw user requirements into a comprehensive, production-ready technical blueprint prior to writing code.

### Criteria for Mastery

- Produces a logical **Sitemap** that accounts for all user journeys and edge-case routing without dead ends.
- Creates structural **Wireframes** identifying layout composition, data inputs, and dynamic interactive states.
- Delivers documentation specifying design tokens (colors, typography scales, spacing tokens) and a modular breakdown of components to be built.

### Assessment Evidence

A "Product Blueprint Dashboard" containing a functional design tool link (e.g., Figma), a comprehensive sitemap schema, and Markdown documentation outlining component specifications.

### Live Check-In Challenges (5 Minutes)

#### Challenge Set A: The Feature Pivot

- **Setup:** The student opens their approved site map and wireframes.
- **Task:** Provide a sudden business requirement change: _"The client just decided that users must be able to filter their dashboard items by date and category simultaneously, rather than just search by keyword. Look at your current component blueprint. Which native components will this change impact, and how will you adjust your data layout to accommodate it?"_
- **What Mastery Looks Like:** The student confidently navigates their architectural plan, isolates the exact component boundaries affected, and verbally outlines the adjusted data and layout flow.

#### Challenge Set B: The Constraint Collapse

- **Setup:** The student displays their wireframes and design tokens (CSS variables).
- **Task:** Provide a sudden environmental constraint: _"Your client just informed you that 40% of their target audience accesses this app on low-end, small-screen mobile devices under bright sunlight. Look at your UI layout blueprints and design tokens. Defend or adjust your choices for color contrast, touch-target sizes, and layout density to prove this design will work for this specific user constraint."_
- **What Mastery Looks Like:** The student references their design token values to verify WCAG contrast ratios (e.g., 4.5:1 or 7:1) and highlights mobile wireframe layouts to verify touch targets meet the minimum 44 x 44 pixel standard.

---

## 2. Component Engineering & Modular Architecture

- **Aligned Course Outcome:** Architect and implement advanced JavaScript patterns, including asynchronous flow and modular architecture.
- **Measurable Description:** The student can encapsulate UI layout, styling, and basic behavior into standalone Native Web Components and decoupled ES Modules, establishing a strict separation of concerns.

### Criteria for Mastery

- Engineers reusable UI blocks utilizing **Custom Elements**, **Shadow DOM** (for absolute style encapsulation), and `<template>` tags.
- Structures application logic cleanly using **ES Modules** (`import`/`export` syntax) to eliminate global scope pollution and tightly coupled dependencies.
- Demonstrates clean separation of concerns, ensuring UI components do not contain hardcoded data logic or external API configurations.

### Assessment Evidence

A component library repository demonstrating native browser-spec encapsulation, zero reliance on external frameworks, and clean modular data boundaries.

### Live Check-In Challenges (5 Minutes)

#### Challenge Set A: The Style Leak

- **Setup:** Provide the student with a component where global CSS is accidentally overriding internal element styling.
- **Task:** _"Global styles are bleeding into this component and breaking its internal layout. Refactor this component to use the Shadow DOM correctly, prove style isolation in the browser DevTools elements panel, and explain why this fixes the leak."_
- **What Mastery Looks Like:** The student successfully instantiates a shadow root (`this.attachShadow({ mode: 'open' })`), appends the template, and demonstrates style isolation using the browser DevTools panel within 3 minutes.

#### Challenge Set B: The Monolithic Split

- **Setup:** Show the student a single, complex JavaScript file containing both UI rendering and helper data utility logic.
- **Task:** _"This file is currently a monolith handling both interface tasks and data transformations. Use ES module syntax to extract the helper code into a separate file, successfully link them using import statements, and verify the app executes flawlessly."_
- **What Mastery Looks Like:** The student cleanly refactors the codebase, exports the targeted functions, handles the relative file path imports accurately, and demonstrates execution without console errors.

---

## 3. Automated Test Engineering

- **Aligned Course Outcome:** Apply automated testing (Unit and Integration) to ensure application logic is bug-resistant.
- **Measurable Description:** The student can author, execute, and debug an automated test suite that strictly validates data transformations, boundary conditions, and state mutations.

### Criteria for Mastery

- Achieves a minimum of **80% statement and branch code coverage** across isolated JavaScript utility and state files.
- Authors strict **Unit Tests** that successfully validate edge cases, boundary conditions, and faulty programmatic inputs.
- Asserts component internal state changes programmatically without relying on manual browser visual verification.

### Assessment Evidence

A green (passing) automated test suite (e.g., Vitest or Jest) executed via a local or continuous integration environment, accompanied by a generated, unmodified coverage report.

### Live Check-In Challenges (5 Minutes)

#### Challenge Set A: The Red-to-Green Break

- **Setup:** Provide the student with an isolated JavaScript utility function (e.g., a data formatter) and one intentionally failing unit test block.
- **Task:** _"Here is a test that is currently failing because the function handles an unexpected input format incorrectly. Analyze the logic, fix either the broken assertion or the utility code, and execute the test runner to achieve a green passing status right now."_
- **What Mastery Looks Like:** The student navigates the testing terminal, modifies the assertions or logic accurately using standard syntax (e.g., `expect().toBe()`), runs the script, and demonstrates a passing suite.

#### Challenge Set B: The False Green

- **Setup:** Provide the student with a passing test suite that passes deceptively (e.g., it passes because it lacks a deep object assertion or relies on a weak truthy check).
- **Task:** _"This test suite is currently green, but it’s a 'false green'—it isn't actually asserting the deep properties of the returned object. Locate the weak assertion, rewrite it to be strict using proper deep comparison, and rerun the suite safely."_
- **What Mastery Looks Like:** The student locates the logical gap in the test file, refactors it to include a strict expectation (e.g., utilizing `toEqual()` instead of a weak check), and reruns the suite to demonstrate true coverage.

---

## 4. Asynchronous Flow & State Management

- **Aligned Course Outcome:** Architect and implement advanced JavaScript patterns, including asynchronous flow and modular architecture.
- **Measurable Description:** The student can orchestrate complex, asynchronous network streams and manage internal client-side state transitions without introducing memory leaks or data race conditions.

### Criteria for Mastery

- Implements reliable **Asynchronous Streams** (via Async/Await and Promises) to process data pipelines smoothly.
- Embeds defensive **Error Handling** that intercepts network dropouts or failed server requests without crashing the browser execution thread.
- Uses modern closure or state object patterns to cleanly update client data layers reactively without polluting the global window scope.

### Assessment Evidence

A fully functional frontend application repository evaluated via strict static code analysis configuration (e.g., ESLint) and an architectural code review log tracking async state modifications.

### Live Check-In Challenges (5 Minutes)

#### Challenge Set A: The Architecture Audit

- **Setup:** The student opens a core logic file from their project where an external API fetch or state change occurs.
- **Task:** _"Trace the lifecycle of this data. If the user's internet drops exactly when they click this button, what happens to the UI state? Show me exactly where in your code that failure is caught, and prove that your user interface reflects this failure gracefully."_
- **What Mastery Looks Like:** The student traces the execution line-by-line, demonstrating clear comprehension of the event loop, promise rejection handling (`try/catch`), and structural encapsulation benefits.

#### Challenge Set B: The State Tracing Game

- **Setup:** The student opens their main JavaScript controller or component state management file.
- **Task:** _"Pick one specific user interaction in your application. Trace the data packet backwards from the initial user event down to the underlying local state store, proving no global scope variables were altered or polluted in the process."_
- **What Mastery Looks Like:** The student cleanly traces data flow across files and modules, validating their understanding of immutable state mutations, reactivity, and DOM updates without global side effects.

---

## 5. Inclusive Craftsmanship & Accessibility (A11y) Compliance

- **Aligned Course Outcome:** Implement A11y patterns to ensure products meet professional WCAG standards.
- **Measurable Description:** The student can evaluate, diagnose, and programmatically adjust web interfaces to fully comply with international accessibility guidelines.

### Criteria for Mastery

- Achieves a **100% automated accessibility score** (via Lighthouse or Axe Core) on all student-built custom components.
- Implements robust **Focus Management** (e.g., focus traps in modal overlays, visible keyboard skip links) verifiable via keyboard-only interactions.
- Maps **Semantic ARIA Attributes** dynamically to custom web components to ensure full screen-reader readability and layout predictability.

### Assessment Evidence

A live production URL submission paired with an accessibility compliance report generated from a manual keyboard navigation verification and automated testing tools.

### Live Check-In Challenges (5 Minutes)

#### Challenge Set A: The Blindfold Test

- **Setup:** The student opens their live web application interface.
- **Task:** _"Put your mouse away. Using only your Tab, Shift+Tab, and Enter/Space keys, navigate to your custom web component, open it, and close it. Prove that focus states remain perfectly visible and do not get trapped in an infinite layout loop."_
- **What Mastery Looks Like:** The component manages focus loops seamlessly without letting focus drop out or disappear. The student explicitly lists which ARIA attributes (such as `aria-expanded` or `aria-controls`) update dynamically in the DOM during the interaction.

#### Challenge Set B: The Accessibility Tree Audit

- **Setup:** The student opens their live application in the browser and opens the DevTools Elements panel.
- **Task:** _"Open the browser's DevTools Accessibility Tree pane for your custom component. Explain to me what the browser sees as the 'Computed Role' and 'Name' of this element. If it says 'generic' or is missing an accessible label, tell me exactly how to fix it in the source."_
- **What Mastery Looks Like:** The student easily navigates the browser's accessibility tree panel, interprets computed accessible properties accurately, and explains how semantic elements or explicit labels expose information to assistive technology.

---

## 6. AI Oversight, Code Auditing & Quality Assurance

- **Aligned Course Outcome:** Evaluate and refine AI-generated test suites and code reviews to ensure technical accuracy.
- **Measurable Description:** The student can act as a technical lead, critically evaluating AI-generated outputs for technical correctness, standard violations, performance bugs, and architectural vulnerabilities.

### Criteria for Mastery

- Identifies and corrects intentional logical flaws, outdated patterns, or vulnerabilities introduced into a code block or test suite.
- Documents an "AI Audit Trail" detailing prompt refinements or manual overrides used to force AI compliance with strict native web specifications.
- Conducts a professional "Pull Request Review" on an AI-generated feature, providing explicit technical justifications for approvals or structural rejections.

### Assessment Evidence

A written code-review portfolio, prompt engineering laboratory journal, or Git Pull Request log displaying the student's manual refactoring decisions and critiques of AI outputs.

### Live Check-In Challenges (5 Minutes)

#### Challenge Set A: Spot the Hallucination

- **Setup:** Display a shared screen showing a short, 15-line block of AI-generated component code containing an explicit native API error or framework abstraction bleed-through.
- **Task:** _"An AI generated this custom component code for you. It looks clean, but it has a significant bug or framework error. Review this code as if you are the Senior Engineer. Find the flaw, tell me why it’s wrong, and state the exact technical feedback or prompt revision you would give back to the AI."_
- **What Mastery Looks Like:** The student rapidly catches the semantic error (e.g., the AI attempted to use a React lifecycle hook inside a native element class, or used a non-existent browser method) and outlines a precise corrective prompt.

#### Challenge Set B: The Prompt Diagnostic

- **Setup:** Display a messy, multi-line monolithic block of code spawned from a poorly phrased prompt.
- **Task:** _"A junior developer wrote this prompt to build a custom tabbed navigation element, and the AI outputted a messy monolith of outdated syntax and inline styles. Diagnose why this prompt failed, and verbally rewrite it using precise engineering vocabulary to force the AI to return clean, native Web Component code."_
- **What Mastery Looks Like:** The student isolates the prompt's structural ambiguity and replaces it using precise engineering terminology (e.g., explicitly demanding "Shadow DOM encapsulation, ES Module patterns for logic, and semantic button targets for keyboard accessibility").
