# Project Foundation

## Project

PsoriaAI

AI-powered psoriasis companion.

This project is being built as a production-style application rather than a tutorial clone.

---

## Goals

1. Learn frontend deeply.
2. Build a portfolio-quality project.
3. Prepare for React + TypeScript.
4. Eventually evolve into a real product.

---

## Development Philosophy

Always think:

Problem
↓

Architecture
↓

Implementation
↓

Review
↓

Git Commit

Never start by writing random code.

Always know WHY a piece of code exists.


# Git Basics

## git init

Creates a Git repository in the project.

---

## git status

Shows the current state of the repository.

Possible states:

Untracked
↓

Tracked
↓

Modified
↓

Staged
↓

Committed

---

## Untracked

Git knows the file exists,
but it is NOT tracking changes yet.

Example:

README.md

index.html

style.css

# Git vs GitHub

Git

- Version Control System
- Runs on your computer
- Tracks changes
- Works offline

GitHub

- Cloud hosting platform
- Stores Git repositories online
- Enables collaboration
- Acts as backup

Relationship

Git can exist without GitHub.

GitHub cannot track versions
without Git.

# Git Commits vs GitHub Contributions

git commit

- Saves changes locally.
- Works without internet.
- Does NOT update GitHub.

------------------------------------

git push

- Uploads commits to GitHub.
- Updates the remote repository.
- Can contribute to the GitHub activity graph.

------------------------------------

Recommended Workflow

Code

↓

git add .

↓

git commit

↓

git push

Rule:

Commit often.
Push after meaningful progress.


# Semantic HTML

Semantic elements describe the purpose of the content.

Examples

<header>

<main>

<footer>

<section>

<article>

<nav>

Using semantic HTML improves:

• Accessibility

• SEO

• Readability

• Maintainability


# Folder Structure

assets/
    images/
    icons/
    fonts/

css/
    reset.css
    variables.css
    style.css
    responsive.css

src/ (future)

README.md

.gitignore

index.html

Folders should represent responsibility,
not convenience.


# Why Use a .container?

Semantic elements describe meaning.

Layout elements control appearance.

<header>
    ↓
Semantic

.container
    ↓
Layout

The container is responsible for:

• max-width

• horizontal padding

• centering

• consistent alignment

The header is responsible for:

• document structure

• accessibility

• page semantics

Rule:

A semantic element answers:

"What is this?"

A layout element answers:

"How should it be displayed?"


