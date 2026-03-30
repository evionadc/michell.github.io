# Data Model: Layout Improvement for Talks and Decks

## Entity: Presentation Deck

**Description**: A complete presentation file that contains all section slides,
navigation affordances, and shared layout patterns for a talk.

**Attributes**:

- `title`: primary talk title
- `sections`: ordered list of deck sections
- `menu_entries`: list of direct navigation targets
- `navigation_mode`: sequential and menu-based navigation behavior
- `layout_rules`: shared visual and structural decisions used across slides

**Relationships**:

- Contains multiple `Slide Section` entities
- Exposes multiple `Theme Menu Entry` entities
- Reuses multiple `Layout Pattern` entities

## Entity: Slide Section

**Description**: A topical portion of the deck that groups one or more slides
under a clear theme and narrative purpose.

**Attributes**:

- `section_name`: displayed topic name
- `section_goal`: purpose of the section in the narrative
- `slide_count`: number of slides in the section
- `entry_point`: menu destination used to access the section
- `content_density`: expected amount of content within the section

**Relationships**:

- Belongs to one `Presentation Deck`
- Uses one or more `Layout Pattern` entities

## Entity: Theme Menu Entry

**Description**: A navigation item that connects the presenter to a specific
deck section.

**Attributes**:

- `label`: visible navigation label
- `target_section`: intended destination
- `summary`: short orientation text
- `slide_index`: destination index or equivalent navigation anchor

**Relationships**:

- Belongs to one `Presentation Deck`
- References one `Slide Section`

## Entity: Layout Pattern

**Description**: A reusable visual structure applied across one or more slides
to organize content consistently.

**Attributes**:

- `pattern_name`: label for the reusable pattern
- `content_role`: intro, card grid, timeline, callout, comparison, menu, etc.
- `hierarchy_rules`: expected prominence of title, subtitle, body, and emphasis
- `spacing_rules`: expected padding and rhythm
- `overflow_behavior`: how content remains reachable when vertical space is low

**Relationships**:

- Can be reused by multiple `Slide Section` entities
- Can appear multiple times within one `Presentation Deck`
