# Template Analysis: GitHub Project Templates
## RPL (Recognition of Prior Learning) Application System

**Author:** Boniface Kabaso
**Date:** March 2026
**Assignment:** Assignment 7 — GitHub Project Templates and Kanban Board Implementation

---

## 1. GitHub Project Templates Comparison

The following table compares four GitHub project templates evaluated for suitability for the RPL Application System.

| Feature / Criteria | Basic Kanban | Automated Kanban | Bug Triage | Team Planning |
|---|---|---|---|---|
| **Default Columns** | To Do, In Progress, Done | To Do, In Progress, Done | Needs Triage, High Priority, Low Priority, Closed | Backlog, Ready, In Progress, In Review, Done |
| **Custom Columns** | Yes — manually added | Yes — manually added | Yes — manually added | Yes — manually added |
| **Automation Features** | None built-in. All card movement is manual. | Issues and PRs auto-move to "In Progress" when opened and to "Done" when closed or merged. | Issues auto-move to "Done" when closed. Labels can trigger triage workflows. | Issues auto-move between columns based on PR status (open, review requested, merged). |
| **WIP Limits** | Not built-in (must be enforced manually) | Not built-in | Not built-in | Not built-in |
| **Issue Linking** | Yes — GitHub Issues can be linked as cards | Yes — GitHub Issues and PRs linked; automation triggers on issue events | Yes — Issues linked; optimised for bug tracking workflows | Yes — Issues and PRs linked with milestone and assignee visibility |
| **Label Support** | Yes | Yes | Yes — pre-configured labels (bug, triage, priority) | Yes — supports custom labels and milestones |
| **Milestone / Sprint Support** | No built-in sprint tracking | Partial — can filter by milestone | No | Yes — designed for sprint/milestone-based planning |
| **Agile Methodology Fit** | Basic — suitable for small personal projects with simple workflows | Good — supports Scrum/Kanban hybrid; automation reduces manual overhead | Low — designed for bug and issue management, not sprint planning | Excellent — designed explicitly for team-based Agile sprint planning |
| **Best Suited For** | Solo projects or very small teams with simple linear workflows | Teams using CI/CD pipelines where PRs and issues drive workflow | QA teams or projects in maintenance phase with many reported bugs | Agile teams running sprints with defined backlogs, reviews, and milestones |
| **Complexity / Setup Effort** | Very low | Low | Low | Medium |

---

## 2. Chosen Template: Automated Kanban

### Justification

After evaluating all four templates, **Automated Kanban** was selected as the foundation for the RPL Application System's GitHub project board, with additional custom columns added to meet the project's specific needs.

**Reasons for selection:**

**1. Automation reduces manual overhead for a solo developer.**
As a solo developer playing all Scrum roles simultaneously (as reflected in the Assignment 6 reflection), manually moving cards between columns introduces friction and risks the board falling out of sync with actual work. The Automated Kanban template auto-moves issues to "In Progress" when a linked branch is opened and to "Done" when a PR is merged — this keeps the board accurate with minimal maintenance effort.

**2. Issue and PR integration aligns with the development workflow.**
The RPL system's Sprint 1 tasks (T-001 to T-017 from Assignment 6) are all linked to GitHub Issues. The Automated Kanban template is built specifically around GitHub Issues and Pull Requests as first-class citizens, meaning every commit, PR, and issue closure automatically reflects on the board.

**3. Extensibility supports custom Agile columns.**
The Automated Kanban template provides a clean three-column starting point (To Do, In Progress, Done) that is easy to extend. Two additional columns — **Testing** and **Blocked** — were added to match the RPL project's QA requirements and to surface impediments visually, which is a core Kanban principle.

**4. Better fit than alternatives.**
- *Basic Kanban* was rejected because the complete lack of automation would require constant manual updates, which is unsustainable even for a solo project.
- *Bug Triage* was rejected because the RPL system is in active development, not maintenance. The triage-focused columns do not map to sprint planning workflows.
- *Team Planning* was considered seriously but rejected because its multi-stage column structure (Backlog, Ready, In Progress, In Review, Done) is designed for larger teams with defined review processes. For a solo developer, the additional columns add complexity without proportional benefit at this stage.

---

## 3. Custom Columns Added

| Column Name | Purpose | Justification |
|-------------|---------|---------------|
| **Testing** | Cards move here after development is complete and before they are marked Done. Unit tests, integration tests, and manual smoke tests are performed in this stage. | Aligns with the Definition of Done from Assignment 6, which requires ≥80% test coverage and staging deployment before a story is closed. Without a visible Testing column, the gap between "built" and "verified" is invisible on the board. |
| **Blocked** | Cards move here when a task cannot progress due to a dependency, technical blocker, or missing information. | A core Kanban principle is making impediments visible so they can be resolved quickly. Without a Blocked column, blocked tasks sit invisibly in "In Progress," making it impossible to distinguish active work from stalled work. |

---

*Document prepared for Assignment 7 — RPL Application System*
*Author: Boniface Kabaso | March 2026*
