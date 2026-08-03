---
name: design-first-product-ui
description: Design product interfaces through a mandatory research, divergent-concept, approval, prototype, implementation, and visual-QA workflow. Use for new web, mobile, or desktop product UI; major visual redesigns; information-architecture or navigation changes; design-system creation; or when a user reports generic AI dashboards, repetitive card grids, form-heavy pages, or repeated visual rework. Produce materially different layout directions and obtain explicit approval before editing the production interface. When a current approved DESIGN.md, Figma, or prototype already covers the requested scope, verify it and implement from that contract instead of repeating exploration. For small copy, spacing, accessibility, or bug fixes that preserve an approved design language, classify the work as a local tweak and use a shortened path.
---

# Design-First Product UI

Prevent expensive UI rework by separating product design decisions from production implementation. Treat aesthetic quality as an approval-dependent product requirement, not a final styling pass.

## Non-negotiable rule

For material UI work, do not edit the production interface until the user explicitly approves a design direction. A theme swap, new color palette, or restyled component library is not approval for an information architecture.

Allowed before approval:

- Read-only product and codebase inspection.
- Reference research with source links.
- Text wireframes and direction comparisons in the conversation.
- Isolated disposable prototypes when the user requests or approves prototype creation.

Not allowed before approval:

- Replacing production layouts, navigation, tokens, or component systems.
- Treating a generated design system as user approval.
- Inferring a positive visual preference only from rejected designs.

For a portable cross-project trigger, use [assets/templates/global-agents-ui-gate.md](assets/templates/global-agents-ui-gate.md) as the concise `AGENTS.md` rule and keep this Skill as the detailed workflow.

## 1. Classify the task

Choose exactly one path and state it.

### Local tweak

Use a shortened path when the change preserves an existing approved visual language: copy, one component state, spacing, accessibility, responsive defects, or a bounded UI bug. Inspect context, implement precisely, and verify the affected viewport and interaction.

### Material UI work

Use the full workflow for new products and pages, major redesigns, navigation or information-architecture changes, new design systems, or repeated dissatisfaction with visual output when no approved design contract covers the work.

### Approved design handoff

When the user asks to implement a current approved `DESIGN.md`, Figma, or prototype that fully covers the requested scope, verify its approval status and completeness, then continue at implementation and visual QA. Do not regenerate directions merely to satisfy the workflow. If the artifact leaves a material decision unresolved, ask about only that decision rather than reopening the entire design.

When uncertain, treat the work as material until evidence shows it is local.

## 2. Inspect before proposing

Read the active instructions and inspect the current product, real rendered UI, core user journey, and relevant existing design artifacts. Look for `DESIGN.md`, Figma links, screenshots, design tokens, component libraries, and prior accepted or rejected directions.

Read these resources as needed:

- For known cross-project taste constraints, read [references/personal-visual-profile.md](references/personal-visual-profile.md).
- For research sources, direction requirements, and tool routing, read [references/research-and-concepts.md](references/research-and-concepts.md).
- For concept and implementation review, read [references/review-rubric.md](references/review-rubric.md).

Separate findings into:

- **Verified**: visible in the product, code, design artifact, or direct user statement.
- **Inferred**: plausible but not yet approved.
- **Unknown**: would materially affect layout, interaction, or visual character.

## 3. Establish the UX brief

Identify before visual exploration:

1. Primary user and their single most important job.
2. Usage frequency, device, environment, and time pressure.
3. Content priority and the decision the first screen must support.
4. Required actions versus secondary or exceptional actions.
5. Desired emotional character and trust level.
6. Positive references and anti-references, including what specifically matters in each.

If a missing answer would materially change the result, ask at most three concise questions. Do not ask the user to select colors or components before the product structure is understood.

Use [assets/templates/ux-brief.md](assets/templates/ux-brief.md) when a durable brief is useful. Keep exploration in the conversation when files would add no value.

## 4. Research real interfaces

Use current, real product references instead of generating styles from adjectives alone. Research the relevant task flow, not only the product category. Cite the source and explain what to borrow and what not to copy.

Collect a small evidence set:

- Two to four positive references for layout, flow, typography, or interaction.
- At least one anti-reference.
- Existing product constraints that make a reference transferable or unsuitable.

Do not present a gallery without analysis. Do not copy a full visual identity or proprietary screen.

## 5. Diverge on structure

Present two or three directions that are materially different in information architecture and interaction model. Do not submit the same sidebar-and-card shell in different colors.

For every direction include:

- Concept name and one-sentence product idea.
- Layout archetype and content hierarchy.
- Primary interaction and navigation model.
- Typography, color behavior, imagery, and motion character.
- Component strategy and what remains hidden until needed.
- Desktop and mobile behavior.
- One memorable design device tied to the product's purpose.
- Tradeoffs, implementation cost, and likely failure mode.
- References and anti-references.

Recommend one direction, but keep the alternatives credible. Use [assets/templates/concept-comparison.md](assets/templates/concept-comparison.md) for durable work.

## 6. Stop at Approval Gate A

Request an explicit choice: approve one direction, combine specified parts, or continue exploration. Do not interpret silence, a positive comment, or approval of one color as approval of the full direction.

Record the approved and rejected decisions. Rejected directions must not silently reappear in later implementation.

## 7. Prototype the selected direction

Choose the lowest-cost artifact that resolves the remaining risk:

- Text wireframe for hierarchy questions.
- Static visual composition for aesthetic questions.
- Clickable isolated prototype for navigation and interaction questions.

Keep prototypes outside production routes and business logic. Use realistic content and test at least one desktop and one mobile viewport. Show the result to the user.

## 8. Stop at Approval Gate B

Before production implementation, obtain explicit approval of the prototype or annotated design specification. If the user rejects it, return to the smallest earlier stage that explains the mismatch.

## 9. Persist the design contract

After approval, adapt [assets/templates/DESIGN.md](assets/templates/DESIGN.md) to the project and save it in the project's established documentation location. If none exists, prefer `docs/DESIGN.md`.

The design contract must capture:

- Product experience and primary journey.
- Approved layout and responsive behavior.
- Visual system and component rules.
- Interaction, motion, accessibility, and content-density rules.
- Positive references, anti-references, and explicit bans.
- Approval date and remaining unknowns.

Do not add unapproved taste assumptions. Project `DESIGN.md` overrides general taste guidance for that project.

## 10. Implement from the contract

Use the approved `DESIGN.md` as the source of truth. Reuse existing product logic and components where they fit; do not let a component library dictate the product's visual identity.

Route optional tools by phase rather than loading every design skill at once:

- Research and UX heuristics: UI/UX research skills and real-interface libraries.
- Concept or prototype: a design-canvas or prototype skill.
- Production implementation: one frontend design skill plus the project's framework guidance.
- Critique and polish: a dedicated audit skill after implementation.
- Browser verification: rendered desktop and mobile interaction, console, overflow, and accessibility checks.

Announce any selected skill and why it is needed. When a tool is unavailable, continue with the same workflow using local artifacts and browser evidence.

## 11. Verify against the approved design

Use [assets/templates/visual-acceptance.md](assets/templates/visual-acceptance.md) to define the receipt. At minimum verify:

- Primary journey and all required states.
- Desktop and mobile layout against the approved direction.
- No horizontal overflow, clipped actions, or hidden essential content.
- Keyboard navigation, focus visibility, semantics, contrast, and reduced motion.
- Realistic empty, loading, error, and populated states.
- No reintroduction of rejected archetypes, colors, density, or microcopy.
- Visual screenshots reviewed against `DESIGN.md`, not only test-suite success.

If implementation materially departs from the contract, either correct it or request approval for a documented design change.

## 12. Preserve preference boundaries

After a successful project, ask before promoting a project-specific choice into the cross-project visual profile. Never silently turn one approved design into the default for every future product.
