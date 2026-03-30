# Tasks: Layout Improvement for Talks and Decks

**Input**: Design documents from `/specs/001-layout-improvements/`  
**Prerequisites**: plan.md (required), spec.md (required for user stories), research.md, data-model.md, quickstart.md

**Tests**: Tests are not requested in the feature specification. Validation is
manual through browser review and quickstart scenarios.

**Organization**: Tasks are grouped by user story to enable independent
implementation and validation of each story.

## Format: `[ID] [P?] [Story] Description`

- **[P]**: Can run in parallel (different files, no dependencies)
- **[Story]**: Which user story this task belongs to (e.g., [US1], [US2], [US3])
- Include exact file paths in descriptions

## Path Conventions

- Static presentation files live at repository root
- Feature documentation lives in `specs/001-layout-improvements/`

## Phase 1: Setup (Shared Infrastructure)

**Purpose**: Prepare the deck and shared files for safe layout iteration

- [x] T001 Review `specs/001-layout-improvements/spec.md`, `specs/001-layout-improvements/plan.md`, and `specs/001-layout-improvements/quickstart.md` to confirm scope and validation flow
- [x] T002 Capture the current navigation and layout touchpoints in `apresentacao-squad-hibrida-agentic-ai.html`
- [x] T003 [P] Review shared entry points in `index.html`, `custom.css`, and `site.css` for reusable layout or navigation impact

---

## Phase 2: Foundational (Blocking Prerequisites)

**Purpose**: Establish shared layout and navigation rules that all user stories depend on

**CRITICAL**: No user story work should begin until this phase is complete

- [x] T004 Define a shared deck-safe viewport strategy in `apresentacao-squad-hibrida-agentic-ai.html` for height limits, overflow handling, and scroll behavior
- [x] T005 Define a reusable navigation pattern in `apresentacao-squad-hibrida-agentic-ai.html` for theme menu access from any slide
- [x] T006 Define reusable section layout rules in `apresentacao-squad-hibrida-agentic-ai.html` for intro blocks, cards, callouts, timelines, and dense-content sections
- [x] T007 Validate that foundational rules remain compatible with static hosting, relative paths, and local file opening in `apresentacao-squad-hibrida-agentic-ai.html`

**Checkpoint**: Foundation ready - user story implementation can now begin

---

## Phase 3: User Story 1 - Present Clear Decks Without Layout Breaks (Priority: P1) MVP

**Goal**: Ensure all essential content remains visible or reachable without broken slide layout

**Independent Test**: Open the squad deck on desktop and laptop-sized viewports
and confirm every slide keeps critical content reachable and visually coherent.

### Implementation for User Story 1

- [x] T008 [US1] Refactor the squad deck slide containers in `apresentacao-squad-hibrida-agentic-ai.html` to keep content reachable at common viewport heights
- [x] T009 [US1] Normalize spacing, hierarchy, and density for intro sections in `apresentacao-squad-hibrida-agentic-ai.html`
- [x] T010 [US1] Normalize spacing and fit behavior for card-heavy sections in `apresentacao-squad-hibrida-agentic-ai.html`
- [x] T011 [US1] Normalize spacing and fit behavior for timeline and callout sections in `apresentacao-squad-hibrida-agentic-ai.html`
- [x] T012 [US1] Validate and tune mobile stacking, reading order, and visibility rules in `apresentacao-squad-hibrida-agentic-ai.html`
- [ ] T013 [US1] Run the manual viewport review from `specs/001-layout-improvements/quickstart.md` for all existing deck sections and record any corrections directly in `apresentacao-squad-hibrida-agentic-ai.html`

**Checkpoint**: User Story 1 should now keep the deck readable and reachable independently

---

## Phase 4: User Story 2 - Navigate by Theme During a Presentation (Priority: P2)

**Goal**: Let the presenter jump between themes from anywhere in the deck

**Independent Test**: From any section slide, use the persistent menu control to
return to the theme menu and jump to another section in no more than 2 interactions.

### Implementation for User Story 2

- [x] T014 [US2] Implement or refine the persistent menu control in `apresentacao-squad-hibrida-agentic-ai.html`
- [x] T015 [US2] Implement or refine the menu slide structure and target links in `apresentacao-squad-hibrida-agentic-ai.html`
- [x] T016 [US2] Ensure local-file-safe navigation logic works for menu return and section jumps in `apresentacao-squad-hibrida-agentic-ai.html`
- [x] T017 [US2] Verify menu labels, section ordering, and presenter orientation copy in `apresentacao-squad-hibrida-agentic-ai.html`
- [x] T018 [US2] Confirm the catalog entry in `index.html` still opens the intended deck entry point after navigation updates

**Checkpoint**: User Stories 1 and 2 should both work independently

---

## Phase 5: User Story 3 - Review and Evolve Layouts with Clear Design Rules (Priority: P3)

**Goal**: Make future layout evolution easier through explicit, reusable design patterns

**Independent Test**: Review the deck and supporting docs to verify a maintainer
can identify reusable layout rules, content density expectations, and navigation behavior without guessing.

### Implementation for User Story 3

- [x] T019 [US3] Document the reusable section pattern decisions in `specs/001-layout-improvements/plan.md` if implementation reveals needed clarifications
- [x] T020 [US3] Align the squad deck section patterns in `apresentacao-squad-hibrida-agentic-ai.html` so future sections can reuse intro, card, timeline, and callout structures
- [x] T021 [US3] Review `apresentacao-aprendizado.html`, `apresentacao-spec.html`, and `apresentacao-squads.html` for opportunities to adopt the same navigation or layout pattern later, and note any no-change decisions in `specs/001-layout-improvements/quickstart.md`
- [x] T022 [US3] Ensure the home and deck relationship remains visually coherent after layout changes by reviewing `index.html`, `site.css`, and `apresentacao-squad-hibrida-agentic-ai.html`

**Checkpoint**: All user stories should now be independently functional

---

## Phase 6: Polish & Cross-Cutting Concerns

**Purpose**: Final consistency and validation across the updated experience

- [x] T023 [P] Clean up duplicated or obsolete layout rules in `apresentacao-squad-hibrida-agentic-ai.html`
- [ ] T024 [P] Review wording and accents for presenter-facing text in `apresentacao-squad-hibrida-agentic-ai.html`
- [ ] T025 Run the full quickstart validation in `specs/001-layout-improvements/quickstart.md`
- [ ] T026 Review `README.md` and update it only if the layout improvement changes how decks are navigated or maintained

---

## Dependencies & Execution Order

### Phase Dependencies

- **Setup (Phase 1)**: No dependencies - can start immediately
- **Foundational (Phase 2)**: Depends on Setup completion - blocks all user stories
- **User Stories (Phase 3+)**: Depend on Foundational completion
- **Polish (Phase 6)**: Depends on all desired user stories being complete

### User Story Dependencies

- **User Story 1 (P1)**: Starts after Foundational - no dependency on other stories
- **User Story 2 (P2)**: Starts after Foundational - depends on US1 layout stability for reliable navigation validation
- **User Story 3 (P3)**: Starts after Foundational - best validated after US1 and US2 are in place

### Within Each User Story

- Shared layout behavior before section-specific tuning
- Section structure before final copy and spacing polish
- Deck navigation before catalog validation
- Story validation before moving to the next priority

### Parallel Opportunities

- T003 can run in parallel with T002
- T023 and T024 can run in parallel during polish
- Review-only tasks touching different files can be split across collaborators once foundational deck rules are settled

---

## Parallel Example: User Story 1

```bash
# After foundational rules are defined:
Task: "Normalize spacing and fit behavior for card-heavy sections in apresentacao-squad-hibrida-agentic-ai.html"
Task: "Normalize spacing and fit behavior for timeline and callout sections in apresentacao-squad-hibrida-agentic-ai.html"
```

---

## Implementation Strategy

### MVP First (User Story 1 Only)

1. Complete Phase 1: Setup
2. Complete Phase 2: Foundational
3. Complete Phase 3: User Story 1
4. STOP and validate readability and content reachability across the target deck

### Incremental Delivery

1. Complete Setup + Foundational
2. Deliver User Story 1 for layout safety
3. Deliver User Story 2 for presenter navigation
4. Deliver User Story 3 for reusable design guidance
5. Finish with polish and full quickstart validation

### Parallel Team Strategy

With multiple collaborators:

1. One collaborator stabilizes foundational deck layout rules
2. One collaborator refines section density and viewport behavior
3. One collaborator validates navigation and catalog integration
4. Final pass is consolidated through shared quickstart validation

---

## Notes

- [P] tasks = different files or non-blocking review work
- [US1], [US2], and [US3] map directly to the user stories in `spec.md`
- Tasks intentionally focus on the squad deck first, while keeping reuse in mind
- Manual review is the acceptance path because the feature specification does not request automated tests
