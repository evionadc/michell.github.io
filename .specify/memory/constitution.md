<!--
Sync Impact Report:
- Version change: 1.1.0 -> 1.2.0
- Modified principles:
  - Storytelling Enxuto -> Narrative First
  - Conteudo Guiado por Narrativa -> Structured Story Flow
  - Identidade Visual Reutilizavel -> Reusable Visual System
  - Acessibilidade Como Base -> Accessibility and Readability by Default
  - Publicacao Estatica e Manutencao Leve -> Static Delivery with Low Operational Friction
- Added principles: None
- Added sections:
  - AI Collaboration Standards
- Removed sections: None
- Templates requiring updates:
  - ✅ reviewed only: .specify/templates/plan-template.md
  - ✅ reviewed only: .specify/templates/spec-template.md
  - ✅ reviewed only: .specify/templates/tasks-template.md
  - ✅ reviewed only: README.md
  - ✅ no command templates present: .specify/templates/commands/
- Follow-up TODOs: None
-->

# Michell Talks Constitution

## Core Principles

### Narrative First
Every page, slide, and content block MUST reinforce a single primary message.
Dense text, decorative UI without meaning, and structure that obscures the key
point MUST be removed or simplified.
Rationale: this repository exists to communicate ideas quickly and clearly in
live talks, async sharing, and iterative content reviews.

### Structured Story Flow
Every presentation MUST follow a recognizable narrative arc: opening, context
or tension, development, and closure. New sections MUST make their role in the
story explicit so presenters can navigate by theme without losing coherence.
Rationale: reusable decks only remain useful when the audience can understand
where they are and why the next slide matters.

### Reusable Visual System
Home, decks, and shared components MUST use coherent tokens for typography,
spacing, contrast, navigation, and emphasis. Variations by topic MAY exist,
but they MUST preserve the same family feel and interaction patterns.
Rationale: the project should feel like one authored system, not a collection
of unrelated files.

### Accessibility and Readability by Default
All screens MUST preserve semantic structure, keyboard-friendly navigation,
strong contrast, responsive behavior, and readable content density across
desktop and mobile. Slides MUST avoid hidden overflow that prevents access to
meaningful content.
Rationale: decks are consumed in different environments, including projection,
laptops, and post-event browsing.

### Static Delivery with Low Operational Friction
The project MUST remain compatible with static hosting on GitHub Pages using
local assets, relative paths, and minimal operational dependencies. Additional
technical complexity SHOULD only be introduced when it materially improves the
authoring or presentation experience.
Rationale: fast publishing and low maintenance are part of the product value.

## Experience Standards

The home page MUST behave as an editorial catalog, not just a link list.
Presentations MUST provide clear orientation, including direct access to major
themes when the deck grows beyond a few slides. Shared patterns such as cover
slides, section intros, navigation affordances, and executive summary blocks
SHOULD remain consistent across decks unless a stronger storytelling reason
requires deviation.

## AI Collaboration Standards

When AI is used to create or revise presentations, prompts, specs, and edits
MUST preserve the human intent of the talk and improve clarity rather than add
volume. AI-generated content MUST be reviewed for narrative fit, visual
coherence, and presenter usability before being accepted. Specifications for
new sections SHOULD capture purpose, audience value, layout expectations,
animation intent, and responsiveness requirements.

## Content Workflow

New talks SHOULD start from reusable structure and explicit section goals.
Draft content MUST be distinguishable from final narrative. Updates to shared
visual language, deck navigation, or editorial framing MUST consider impact on
the home page and existing presentations.

## Technologies Utilized

The project uses static HTML, CSS, and JavaScript, with Reveal.js powering the
presentation decks. Hosting and distribution happen through GitHub Pages
without a required build pipeline.

## Development Process

Changes MUST prioritize direct edits to the static repository files. Before
publishing, every meaningful change SHOULD verify:

- narrative clarity for the changed deck or page
- visual consistency across home and presentations
- navigation paths and menu shortcuts working as expected
- responsive behavior and readable content density
- no critical content hidden by overflow, viewport limits, or animation timing
- placeholders clearly marked when final content is not yet available

## Governance

This constitution overrides local preferences for presentation structure,
navigation, and shared visual behavior. Any amendment MUST document its impact
on storytelling, maintainability, static delivery, and AI-assisted workflow.
Versioning follows semver:

- MAJOR: incompatible redefinition or removal of a governing principle
- MINOR: new normative guidance or material expansion of existing rules
- PATCH: clarification, wording, or non-semantic cleanup

Compliance reviews MUST happen whenever shared layout behavior, deck navigation,
content workflow, or AI authoring expectations are materially changed.

**Version**: 1.2.0 | **Ratified**: 2026-03-27 | **Last Amended**: 2026-03-30
