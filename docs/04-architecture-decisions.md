# Architecture Decisions

## ADR-001

Decision:
Use semantic HTML.

Reason:
Improves accessibility, SEO and maintainability.

Status:
Accepted

-------------------------------------

## ADR-002

Decision:
Use TypeScript for PsoriaAI.

Reason:
Better scalability, type safety and React integration.

Status:
Accepted

-------------------------------------

## ADR-003

Decision:
Organize CSS into reset.css,
variables.css and style.css.

Reason:
Single responsibility and maintainability.

Status:
Accepted


## ADR-004

Decision:
Organize design tokens into categories.

Categories:

- Colors
- Typography
- Spacing
- Border Radius
- Shadows

Reason:
Improves readability and scalability as the project grows.

Status:
Accepted


-------------------------------------

## ADR-005

Decision

Separate project documentation
from engineering notes.

Reason

Project knowledge and learning notes
serve different purposes.

Status

Accepted

-------------------------------------

## ADR-006

Decision

Use semantic HTML before styling.

Reason

Accessibility and maintainability
should be established before visual design.

Status

Accepted

-------------------------------------

## ADR-007

Decision

Adopt a documentation-first workflow.

Reason

Document major architectural decisions
as they are made instead of relying on memory.

Status

Accepted

-------------------------------------

## ADR-008

Decision

Use purpose-based naming
instead of implementation-based naming.

Examples

hero-content

feature-card

Instead of

left-box

blue-button

Reason

Names should remain meaningful
even when the layout changes.

Status

Accepted



### 2. `docs/04-architecture-decisions.md` — one small decision

This one is worth recording because it's an actual **design/implementation decision**, not just CSS syntax:

```md
## Responsive How It Works Layout

Decision:
Use a 3-column step layout above 768px and a single-column vertical
journey at 768px and below.

Reason:
The desktop layout communicates the three-step journey horizontally.
On smaller screens, stacking the steps improves readability while
preserving the journey through vertical connectors.

Implementation:
Use `.step:not(:last-child)::after` for decorative connectors rather
than adding connector elements to the HTML.


