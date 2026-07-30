# Information Architecture (IA)

Before writing HTML, decide the order of information.

Users don't read a webpage randomly.

They follow a journey.

Good HTML begins with a good information architecture.

Think in sections first,
tags second.


# id vs class

Use class for:

- Styling
- Reusable components
- Layout
- Component architecture

Use id for:

- Unique page sections
- Anchor navigation
- Accessibility relationships
- JavaScript when uniqueness matters

Rule:

Classes describe WHAT something is.

IDs identify WHICH specific element it is.


# Every <div> Needs a Job

Before adding a div, ask:

Why does this div exist?

Valid reasons:

- Layout
- Flex/Grid wrapper
- Container
- Grouping related content

Invalid reason:

"I always add a div."

Rule:

Every div should have a responsibility.

If it has no responsibility,
it probably shouldn't exist.


# <header> vs <nav>

<header>

Represents the introductory content of a page or section.

Typical content:

- Logo
- Site title
- Navigation
- Search
- Hero intro (sometimes)

------------------------------------

<nav>

Represents a navigation landmark.

Typical content:

- Main navigation
- Sidebar navigation
- Footer navigation
- Table of contents

------------------------------------

Rule

A <nav> often lives inside a <header>,
but it is not required to.

Choose the placement based on the page's structure,
not because "HTML says so."


# Types of Wrappers

1. Semantic Wrapper

<header>

<main>

<section>

<footer>

Purpose:
Describe meaning.

------------------------------------

2. Layout Wrapper

.container

.header-container

.hero-content

Purpose:
Control width, spacing and alignment.

------------------------------------

3. Implementation Wrapper

.feature-grid

.card-row

.stats-grid

Purpose:
Create a specific layout using
Flexbox or Grid.

Rule:

Never create a wrapper without knowing
its responsibility.


# Navigation Design

The navbar should answer:

"What does a first-time visitor need?"

Navigation is not a sitemap.

It is a guide.

------------------------------------

Good navigation:

• Simple

• Focused

• User-oriented

------------------------------------

Ask before adding an item:

Does this help a new visitor
understand the product?

If not,
it probably belongs somewhere else.


# Hero Section

A good Hero answers three questions
within 3–5 seconds.

1. What is this?

Example:
AI-powered psoriasis companion.

------------------------------------

2. Why should I care?

Example:
Track symptoms, understand flare patterns
and access affordable guidance.

------------------------------------

3. What should I do next?

Example:
Begin Your Wellness Journey

------------------------------------

Rule:

Clarity first.

Curiosity second.


