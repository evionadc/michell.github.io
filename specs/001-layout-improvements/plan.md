# Implementation Plan: Layout Improvement for Talks and Decks

**Branch**: `001-layout-improvements` | **Date**: 2026-03-30 | **Spec**: [spec.md](D:/projeto_apresentacao/michell.github.io/specs/001-layout-improvements/spec.md)
**Input**: Feature specification from `/specs/001-layout-improvements/spec.md`

## Summary

Improve the layout system of the presentation catalog and Reveal.js decks so
that slides remain readable across viewport sizes, theme navigation is always
accessible, and new sections can reuse a clearer visual and structural pattern.
The approach keeps the static HTML/CSS/JS architecture, strengthens navigation,
and normalizes overflow, spacing, hierarchy, and reusable section patterns.

## Technical Context

**Language/Version**: HTML5, CSS3, vanilla JavaScript  
**Primary Dependencies**: Reveal.js  
**Storage**: N/A  
**Testing**: Manual browser validation across desktop and mobile viewports  
**Target Platform**: Static web pages in modern desktop and mobile browsers  
**Project Type**: static presentation site  
**Performance Goals**: theme navigation available within 2 interactions; all
critical slide content reachable during manual review  
**Constraints**: GitHub Pages compatibility, relative paths only, no required
build pipeline, no hidden critical content at common viewport heights  
**Scale/Scope**: one target deck plus shared patterns reusable for other talks

## Constitution Check

*GATE: Must pass before Phase 0 research. Re-check after Phase 1 design.*

- Narrative First: PASS. The work improves message clarity by reducing clipped
  content and making section structure easier to follow.
- Structured Story Flow: PASS. The plan adds and preserves navigation by theme,
  supporting non-linear presenter movement without losing context.
- Reusable Visual System: PASS. The plan formalizes reusable patterns for menu,
  cards, timeline, overflow, and section composition.
- Accessibility and Readability by Default: PASS. The work explicitly addresses
  readability, viewport fit, visible content, and responsive behavior.
- Static Delivery with Low Operational Friction: PASS. The plan remains within
  static HTML/CSS/JS and Reveal.js, with no new operational dependency.

Post-design re-check expectation: PASS if artifacts keep static delivery,
maintain clear navigation, and avoid implementation choices that increase
operational friction.

## Project Structure

### Documentation (this feature)

```text
specs/001-layout-improvements/
├── plan.md
├── research.md
├── data-model.md
├── quickstart.md
└── tasks.md
```

### Source Code (repository root)

```text
apresentacao-squad-hibrida-agentic-ai.html
index.html
apresentacao-aprendizado.html
apresentacao-spec.html
apresentacao-squads.html
site.css
custom.css
reveal/
```

**Structure Decision**: The feature is implemented directly in the existing
static presentation files at repository root, with the squad deck as the first
target and shared layout decisions intended for reuse across other decks.

Reusable pattern decisions captured during implementation:

- theme navigation must target semantic deck sections rather than fragile
  hard-coded slide indexes when possible
- slide containers must preserve access to critical content through bounded
  height and internal scrolling
- dense section types require local tuning while still inheriting the same
  design system tokens and navigation behavior

## Complexity Tracking

No constitution violations currently require justification.
