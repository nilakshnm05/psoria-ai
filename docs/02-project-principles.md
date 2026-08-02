# Project Principles

## HTML

Semantic first.

Never use a div when a semantic element exists.

---

## CSS

Use design tokens.

Avoid hardcoded values.

Organize by responsibility.

---

## Git

One meaningful feature

↓

One commit

↓

One push

---

## Components

Single responsibility.

Reusable before duplicated.

---

## Code Quality

Readable over clever.

Consistency over shortcuts.


## CSS File Order

1. reset.css

Removes browser defaults.

-------------------------

2. variables.css

Defines reusable design tokens.

-------------------------

3. style.css

Implements the application's styles.

-------------------------

4. responsive.css

Overrides styles for different screen sizes.

-------------------------

Rule

Build from foundation to specialization.

Each file depends on the layer before it.



---

## Naming

Use names that describe purpose,
not appearance.

Good

hero-content

feature-card

Bad

left-box

blue-button

working-div

---

## Documentation

Important architectural decisions
must be documented.

Every feature should be understandable
without reading the entire codebase.

---

## Design System

Avoid hardcoded reusable values.

Every reusable value should become
a design token.

Examples

- Colors

- Typography

- Spacing

- Radius

- Shadows

---

## Learning Philosophy

Understand first.

Implement second.

Memorize last.

Every implementation should answer:

Why does this exist?


