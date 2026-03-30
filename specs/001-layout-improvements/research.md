# Research: Layout Improvement for Talks and Decks

## Decision 1: Keep the solution inside the static Reveal.js deck architecture

**Decision**: Use HTML, CSS, and lightweight deck-level JavaScript only.

**Rationale**: The project constitution requires static delivery with low
operational friction. The current stack already supports the needed outcomes:
navigation by theme, responsive layout behavior, and improved readability.

**Alternatives considered**:

- Introduce a build step for templating
- Migrate the deck into a component framework
- Use an external runtime for layout orchestration

## Decision 2: Treat overflow as a first-class presentation behavior

**Decision**: Design slides to fit common presenter viewports by default, while
allowing graceful internal scrolling when content exceeds safe vertical space.

**Rationale**: Presentation content varies by section density. A layout system
that assumes all content always fits creates clipping risk. Controlled overflow
preserves access to critical information without requiring deck fragmentation
for every dense section.

**Alternatives considered**:

- Force every slide to fit with no overflow handling
- Split every dense section into multiple smaller slides
- Allow browser-level page overflow outside the slide container

## Decision 3: Use a persistent menu pattern for presenter navigation

**Decision**: Provide a menu slide and a persistent action that returns the
presenter to the menu from any section.

**Rationale**: Large decks need non-linear movement during live presentation.
Menu-based navigation supports presenter control and aligns with the
constitution requirement for clear orientation when decks expand.

**Alternatives considered**:

- Rely only on sequential next/previous navigation
- Use only keyboard shortcuts with no visible affordance
- Duplicate navigation controls per section without a central hub

## Decision 4: Standardize reusable section patterns

**Decision**: Organize sections around repeatable pattern families: intro,
definition cards, comparison cards, timelines, strategic grids, and highlighted
callouts.

**Rationale**: Reuse lowers maintenance cost, reduces layout drift, and makes
future section authoring more predictable.

**Alternatives considered**:

- Design each section independently
- Use one universal pattern for all sections regardless of content type
- Keep current ad hoc section-specific layout rules

## Decision 5: Apply UI/UX review criteria from executive presentation design

**Decision**: Evaluate layouts using hierarchy, scanability, spacing rhythm,
viewport fit, keyboard-friendly navigation, and clear presenter affordances.

**Rationale**: The deck is both a live-presentation tool and an async reading
experience. Executive presentation quality depends on fast comprehension,
visible structure, and minimal friction.

**Alternatives considered**:

- Focus only on visual aesthetics
- Treat the deck as a pure slideshow with no navigation expectations
- Optimize only for desktop projection without considering later browsing
