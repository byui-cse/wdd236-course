# Patterns and questions for WDD 236

Use only the patterns relevant to the feature under investigation. Slice IDs below are orientation aids from the course at skill creation; confirm names and expectations against the current student-facing Competency Guide when available. These are practice prompts, not additional assessment requirements.

## Pattern vocabulary

| Pattern | Look for | Ask about purpose or evidence | Try a relevant variation |
| --- | --- | --- | --- |
| Event → state change → render | Listener registration, state owner, update path, DOM changes | Why is this state owned here? What keeps two views consistent? | Two components display the same item |
| Fetch → check → transform → display | Request, status/shape checks, mapping, consumer | Where does external data become safe for this interface to use? | Unexpected response shape or non-success status |
| Loading / success / empty / error | Explicit state transitions and their UI representations | What prevents a stale spinner or an empty result appearing as failure? | Empty results followed by a failed request |
| Latest request wins | Cancellation or response identity/version checks | Can an older response overwrite a newer selection? | Delay the first of two requests |
| Register → handle → clean up | Lifecycle setup and teardown, listener/subscription identity | What survives removal? What is registered on reconnection? | Remove and reinsert the element |
| Public input / output boundary | Attributes, properties, events, module exports | Why use this interface instead of modifying another component's internals? | Reuse the component in a second context |
| Validate → restore → fallback | Storage read, parsing, shape checks, defaults | Which stored values are trusted, and why? | Missing or malformed saved data |
| Semantic control → exposed state | Native element, accessible name, synchronized properties | What can keyboard and assistive-technology users discover and operate? | Toggle twice using only the keyboard |
| Open → move focus → close → restore focus | Focus destination, dismissal path, return target | Why should focus move here? Where does it return? | Dismiss with the keyboard; remove the original opener |
| Token → component style | CSS custom properties, consuming rules, overrides | Which visual decision is shared? How do you know the intended token applies? | Long content, zoom, theme change, narrow viewport |
| Arrange → act → assert | Setup, meaningful action, observable result | Would this test fail if the behavior were broken? | Change the relevant behavior in a controlled experiment |
| Measure → change → compare | Baseline, targeted change, comparable conditions | What evidence attributes the improvement to this change? | Repeat under the same throttling and cache conditions |

Do not prescribe these as mandatory architecture. Local state can be appropriate; not every application needs a store, subscriptions, cancellation, or persistence. A pattern's presence is not evidence that it is needed or implemented correctly.

## Competency connections

| Slices | Investigate | Example defense question | Evidence to seek |
| --- | --- | --- | --- |
| 1.3, 1.5, 1.6: interaction states, inventory, change impact | Whether the implementation matches the planned responsibilities and states | If a second view needs this feature, which boundaries would change? | Blueprint-to-code mapping and a concrete impact explanation |
| 1.4, 5.2: design tokens and visual accessibility | The rules producing the visual result under constraints | Which rule prevents this content from becoming unusable at a narrow width? | Computed styles, reflow/zoom observation, relevant measurements |
| 2.1–2.5: custom elements, templates, encapsulation, modules, separation | Component contracts and lifecycle responsibilities | What makes this component reusable outside this page? | Inputs/events, registration, lifecycle code, reuse experiment |
| 3.2–3.5: logic, assertions, state and workflow tests | Whether assertions establish the intended behavior | Could this remain green if no state change happened? | Relevant assertions, observed run, meaningful negative case |
| 4.1–4.7: async and state | Data ownership, ordering, failure, recovery, persistence | What if this response arrives after a newer one? | Request/state sequence and a controlled observation |
| 5.1, 5.3–5.7: semantics, keyboard, focus, ARIA, tree, audits | Whether users can discover and operate the behavior across states | What supports the claim that this interaction is accessible? | Semantics, computed name/role/state, keyboard/focus checks; manual audit limits |
| 6.2–6.6: AI review and verification | Evidence behind accepting or rejecting generated code | What AI suggestion did you question, and what resolved the question? | Source, current documentation where needed, focused experiment, remaining risk |
| 7.4–7.5: optional performance | Work on the relevant path and measured bottlenecks | Why optimize this operation first? | Baseline, justified intervention, comparable measurements |

Avoid broad conclusions from narrow observations: a `catch` does not prove recovery; Shadow DOM does not prove every boundary is appropriate; an ARIA attribute does not prove usable accessibility; a passing assertion does not prove a complete workflow; a smaller file does not prove faster interaction.

## Example investigation: saving a trail

This is hypothetical. Inspect the actual student's source before using its architecture or names.

A possible path is: native Save button → card handler → `trail-save` event → application listener → saved-trails state → card property update → visual and accessible state updates.

For guided practice, initially show the button, card, application listener, and state owner without completing all arrows. Ask: "Where do you expect the saved value to live, and what code would help us check?" Wait before revealing the path.

Possible later challenge: "Two cards represent the same trail. Predict what changes in the second card after saving the first." A valid outcome may reveal a design limitation rather than a bug against the current specification. Ask the student to distinguish those cases.

If an event must cross a shadow boundary, inspect where it is dispatched, where the listener is registered, and whether propagation options support that relationship. Do not assert that every custom event always needs the same options.
