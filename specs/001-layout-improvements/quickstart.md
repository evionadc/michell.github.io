# Quickstart: Layout Improvement for Talks and Decks

## Goal

Validate that the squad deck layout remains readable, navigable, and reusable
after the planned improvements.

## Preparation

1. Open `apresentacao-squad-hibrida-agentic-ai.html` in a browser.
2. Review the deck both from a local file and from the static-served version if
   available.
3. Prepare at least two viewport sizes:
   - desktop or laptop presentation size
   - narrow mobile-sized viewport

## Validation Flow

1. Open the menu slide and confirm every major theme is listed clearly.
2. Enter each section directly from the menu and verify the destination is
   correct.
3. From each section, use the persistent menu control to return to the menu.
4. Review every slide for:
   - clipped endings
   - hidden callouts
   - inaccessible text near the bottom
   - visual hierarchy that feels weaker than neighboring slides
5. Review dense slides and confirm all critical content remains reachable.
6. Repeat a shorter pass on mobile width and verify reading order and menu
   access remain intact.

## Expected Result

- No slide hides critical content
- Theme navigation works in both directions
- Section structures feel visually related
- Dense slides remain usable instead of visually breaking
- The deck stays compatible with static hosting and local opening

## Reuse Notes

- `apresentacao-squad-hibrida-agentic-ai.html` is the first deck to adopt the
  persistent menu pattern, scroll-safe slide shell, and denser section-specific
  layout tuning.
- `apresentacao-aprendizado.html`, `apresentacao-spec.html`, and
  `apresentacao-squads.html` were reviewed as potential follow-up candidates for
  the same navigation and overflow pattern, but were not changed in this
  feature to keep the implementation focused on the target deck.
- `index.html` remains the launch point for the deck and should continue to be
  reviewed whenever menu entry behavior or deck naming changes.
