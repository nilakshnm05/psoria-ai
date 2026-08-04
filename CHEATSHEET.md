# Frontend Cheatsheet

## HTML

Semantic > Div

Container controls layout

Class = reusable

ID = unique

---

## CSS

border-box

Design Tokens

Specificity

ID > Class > Element

Reset → Variables → Style → Responsive

---

## Git

status

↓

add

↓

commit

↓

push

---

## Rule

Understand first.

Implement second.

Container

Shared layout utility

Responsibilities

- max-width
- horizontal padding
- centering

Component class

Responsible for section-specific layout only.


## Parent vs Child Responsibilities

Parent
- Controls layout
- display
- gap
- align-items
- justify-content

Child
- Controls its own content
- typography
- internal flex direction
- spacing between its own children

Example

.hero-container
↓

Controls

.hero-content
.hero-preview

.hero-content
↓

Controls

.hero-text
.hero-actions
.hero-trust