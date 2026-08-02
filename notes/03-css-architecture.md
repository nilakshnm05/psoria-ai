# Design Tokens

A design token is a reusable value used across the application.

Examples

Colors

Spacing

Font sizes

Border radius

Shadows

------------------------------------

Why use them?

Single source of truth.

Change once.

Update everywhere.

Improves:

• Consistency

• Maintainability

• Scalability

------------------------------------

Rule

Never hardcode values that are likely
to be reused.


# Why CSS Reset Exists

Every line in reset.css must remove a browser assumption.

Reset files should not contain design decisions.

Browsers ship with a User Agent Stylesheet.

This gives HTML elements default styles.

Examples

• h1 has margins

• p has margins

• ul has padding

• buttons have default appearance

Different browsers may apply these styles differently.

------------------------------------

CSS Reset

Removes browser defaults.

Creates a consistent starting point.

Rule

Always start from a predictable baseline.

# Responsibilities of CSS Files

reset.css

Purpose:

Remove browser defaults.

Examples

• margin

• padding

• box-sizing

• lists

• images

• links

-------------------------

variables.css

Purpose:

Store reusable design tokens.

Examples

• colors

• spacing

• typography

• border radius

-------------------------

style.css

Purpose:

Style the application.

Rule

Every CSS file should have one clear responsibility.

# box-sizing

content-box (default)

Width applies only to the content.

Total size grows when padding and border are added.

------------------------------------

border-box

Width applies to the entire element.

Padding and border are included inside the specified width.

------------------------------------

Why use border-box?

• Predictable layouts

• Easier responsive design

• Matches component thinking

Rule

Think about the size of the whole component,
not just the content.

# Padding vs Width

If content feels cramped, first identify WHY.

Case 1:
Text is too close to the edges.

→ Increase padding.

Case 2:
Content area is too small because padding is excessive.

→ Decrease padding.

Changing width affects the overall layout and should usually be the last option.

Rule:

Adjust internal spacing before changing component dimensions.

# Organizing reset.css

Two styles are both valid.

Option A

One block for everything.

Option B

Separate blocks by responsibility.

Example

* {
    margin: 0;
    padding: 0;
}

*,
*::before,
*::after {
    box-sizing: border-box;
}

Both work.

Option B improves readability because each block has one clear purpose.

Rule:

Organize CSS by responsibility, not just correctness.


----------------------------------------------------

# CSS Cascade

When multiple rules match an element,
the browser chooses the winner using:

1. Importance

2. Specificity

3. Source Order

Rule

Specificity beats order.

Order matters only when specificity ties.

----------------------------------------------------

# Specificity

Element

↓

Class

↓

ID

More specific selectors
override less specific ones.

----------------------------------------------------

# CSS Architecture

Professional CSS should be layered.

reset.css

↓

variables.css

↓

style.css

↓

responsive.css

Each layer depends
on the previous one.

----------------------------------------------------

# Design Tokens

Good

--color-primary

--spacing-lg

--radius-md

Bad

--blue

--20px

Rule

Name tokens by purpose,
not implementation.

----------------------------------------------------

# Variables

Store reusable values inside

:root

Access them using

var(--token-name)

Benefits

- Single source of truth

- Easier maintenance

- Consistency

----------------------------------------------------

# Design System Thinking

A design system is a collection of
reusable visual rules.

Examples

Colors

Typography

Spacing

Buttons

Cards

Icons

Rule

Build components,
not isolated pages.


# Global Body Styles

The body element acts as the canvas for the application.

Typical responsibilities:

- Background color
- Default text color
- Global typography
- Base font size
- Line height
- Minimum page height

Rule

Global styles should establish defaults for the entire application.

Component-specific styles belong in their respective selectors.


# Class Composition

An element can have multiple classes.

Example

<div class="container hero-container highlighted">

The browser applies styles from all matching classes.

If multiple classes define different properties,
the properties are combined.

If multiple classes define the same property,
the CSS Cascade determines the winner.

Benefits

- Reusable styles
- Single Responsibility
- Less duplication
- Better scalability

Rule

Compose small reusable classes instead of creating one large class.


# Class Composition and the Cascade

An element can have multiple classes.

Each matching class contributes its styles.

If different classes define different properties,
the browser combines them.

If different classes define the same property,
the CSS Cascade decides the winner.

The cascade considers:

1. Importance
2. Specificity
3. Source order

Rule

Multiple classes work together until they define the same property.
When they conflict, the cascade resolves the conflict.


# Reusable Layout Classes

A reusable class contains shared layout rules.

Example

.container

Responsibilities

- Controls maximum width
- Centers content
- Adds horizontal spacing

Section-specific layout belongs in dedicated classes such as:

- .header-container
- .hero-container
- .footer-container

Rule

Separate shared layout from component-specific layout.


# Logical Properties

Modern CSS provides logical properties that replace
physical directions.

Examples

padding-block

↓

padding-top + padding-bottom

----------------------------------

padding-inline

↓

padding-left + padding-right

----------------------------------

margin-block

↓

margin-top + margin-bottom

----------------------------------

margin-inline

↓

margin-left + margin-right

Benefits

- Cleaner syntax
- Better internationalization support
- More maintainable layouts

Rule

Prefer logical properties in new projects unless
there is a specific reason to use physical directions.


## Responsibility Before Rules

Before adding a CSS property, ask:

"Which class owns this responsibility?"

Example

.container

- Width
- Centering
- Horizontal spacing

.header-container

- Flex layout
- Vertical spacing
- Header-specific alignment

Rule

Avoid giving two classes responsibility for the same concern.




