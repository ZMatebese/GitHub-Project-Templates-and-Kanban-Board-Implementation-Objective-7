# Kanban Board Explanation
## RPL (Recognition of Prior Learning) Application System

**Author:** Boniface Kabaso
**Date:** March 2026
**Assignment:** Assignment 7 — GitHub Project Templates and Kanban Board Implementation

---

## 1. What is a Kanban Board?

A Kanban board is a visual project management tool that represents work as cards moving through a series of columns, where each column corresponds to a stage in the development workflow. The word "Kanban" comes from Japanese, meaning "visual signal" or "card" — the core idea being that the state of all work is always visible at a glance to everyone involved.

Unlike a simple to-do list, a Kanban board shows not just *what* needs to be done, but *where every task currently is* in the process, *who is working on it*, and *whether anything is blocked*. This makes it a powerful tool for identifying bottlenecks, balancing workload, and maintaining a continuous flow of completed work.

---

## 2. The RPL System Kanban Board

### Board Columns and What They Represent

The RPL Application System's Kanban board uses the following five columns:

| Column | Meaning | WIP Limit |
|--------|---------|-----------|
| **To Do** | Tasks from the Sprint 1 backlog that have not yet been started. All 17 Sprint 1 tasks begin here. | No limit — this is the input queue. |
| **In Progress** | Tasks actively being worked on right now. A card moves here the moment a developer starts a linked branch. | **Max 3 tasks** — enforced manually to maintain focus. |
| **Blocked** | Tasks that cannot progress due to a dependency, missing information, or technical impediment. Requires a comment explaining the blocker. | No limit — all blockers must be visible. |
| **Testing** | Tasks where development is complete and the feature is being tested (unit tests, integration tests, manual smoke testing on staging). | **Max 3 tasks** — mirrors the In Progress limit to avoid testing becoming a backlog. |
| **Done** | Tasks where all acceptance criteria are met, tests pass, code is merged to main, and the feature is deployed to staging. Auto-populated by GitHub automation when a PR is merged. | No limit. |

---

## 3. How the Board Visualises Workflow

Each task from the Sprint 1 plan (Assignment 6, T-001 to T-017) is represented as a GitHub Issue card on the board. Cards are colour-coded using GitHub labels:

| Label | Colour | Meaning |
|-------|--------|---------|
| `feature` | Green | A new functional capability being built |
| `infrastructure` | Blue | Setup, CI/CD, database, or DevOps tasks |
| `security` | Red | Tasks related to encryption, RBAC, or access control |
| `testing` | Yellow | Test writing and QA tasks |
| `bug` | Orange | Defects discovered during testing |

Cards display: task title, assigned developer (@mention), linked user story ID (e.g., US-001), and story points. This means anyone viewing the board can immediately understand what is being built, by whom, and how it connects to the product backlog.

---

## 4. How the Board Limits Work-in-Progress (WIP)

WIP limits are one of the defining features of Kanban. Without them, a developer (or team) can start many tasks simultaneously, creating an illusion of progress while nothing actually gets finished. The RPL board enforces a **WIP limit of 3 tasks in the "In Progress" column** and **3 tasks in the "Testing" column**.

In practice this means:
- If three tasks are already In Progress and a new task is tempting to start, the Kanban rule is to first finish or unblock one of the existing tasks before pulling a new card.
- If the Testing column fills up, development must pause and focus on clearing tested items to Done before new development tasks can be moved to Testing.

For a solo developer, this discipline is especially important because the temptation to context-switch between many parallel tasks is high. The WIP limit enforces the principle of *stop starting, start finishing*.

---

## 5. How the Board Supports Agile Principles

| Agile Principle | How the RPL Kanban Board Supports It |
|-----------------|--------------------------------------|
| **Working software over comprehensive documentation** | The board tracks tasks that produce runnable, testable code — not documentation milestones. The Definition of Done requires deployed, tested features. |
| **Responding to change** | New tasks or reprioritised stories can be added to the backlog (To Do) at any time. The board does not lock in a rigid sequence. |
| **Continuous delivery** | The Testing → Done flow ensures features are verified and merged continuously rather than in a big-bang release at the end. |
| **Transparency and inspection** | The board gives a real-time, honest picture of where work stands — including blocked tasks — enabling rapid identification of problems. |
| **Sustainable pace** | WIP limits prevent overcommitment and ensure the developer is not juggling more tasks than can be handled effectively. |

---

## 6. README Section: Kanban Board Customisation Choices

The following text is intended for inclusion in the project's GitHub repository README.md:

---

### 📋 Project Kanban Board

This project uses a customised **Automated Kanban** board on GitHub Projects to manage Sprint 1 development of the RPL Application System.

**Board URL:** [RPL System — Sprint 1 Board](https://github.com/[your-username]/[your-repo]/projects/1)

**Custom Columns Added:**
- **Testing** — Added to align with our Definition of Done, which requires all features to pass unit and integration tests before being marked complete. This makes the QA stage visible and prevents untested code from being marked Done.
- **Blocked** — Added to surface impediments immediately. Any task that cannot progress is moved here with a comment explaining the blocker, ensuring no task silently stalls in "In Progress."

**WIP Limits:**
- In Progress: maximum 3 tasks
- Testing: maximum 3 tasks

**Labels in use:** `feature`, `infrastructure`, `security`, `testing`, `bug`

All cards on the board are linked to GitHub Issues, which are in turn linked to user stories from the product backlog (see `AGILE_PLANNING.md`).

---

*Document prepared for Assignment 7 — RPL Application System*
*Author: Boniface Kabaso | March 2026*
