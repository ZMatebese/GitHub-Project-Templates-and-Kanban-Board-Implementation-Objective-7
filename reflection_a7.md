# Reflection: Challenges in Selecting and Customising the GitHub Kanban Template
## RPL (Recognition of Prior Learning) Application System

**Author:** Boniface Kabaso
**Date:** March 2026
**Assignment:** Assignment 7

---

## Lessons Learned

Working through Assignment 7 gave me hands-on experience with GitHub Projects as a project management tool, and it surfaced a number of genuine challenges — both in selecting the right template and in thinking critically about how Kanban boards compare to other tools I have encountered.

**Choosing the Right Template Was Not Obvious**

My first instinct was to select the Team Planning template because it has the most columns by default and looked the most "complete." But after mapping my Sprint 1 tasks from Assignment 6 onto it, I realised that its multi-stage column structure (Backlog, Ready, In Progress, In Review, Done) was designed for teams where different people perform different roles — a developer moves a card to "In Review" and a different person performs the review. As a solo developer, the "In Review" column would have remained permanently empty, creating a misleading picture of the workflow. This taught me that a template's visual complexity is not the same as its suitability — the right template is the one that maps accurately to the actual workflow, not the most impressive-looking one.

**Customising Columns Required Thinking About What Makes Work Visible**

Adding the "Blocked" and "Testing" columns forced me to think carefully about what information a Kanban board should make visible. The default three-column Kanban (To Do, In Progress, Done) hides two important states: work that is waiting to be verified, and work that cannot proceed. In a team environment, a blocked task sitting in "In Progress" looks the same as an active task — which means the impediment is invisible until a standup or check-in reveals it. Adding a dedicated "Blocked" column with a mandatory comment explaining the blocker turns an invisible problem into a visible one that demands resolution. This was one of the most practically valuable insights from the assignment.

**GitHub Projects vs. Trello and Jira**

Comparing GitHub Projects to other tools I have used or studied helped clarify its strengths and limitations. Trello is arguably the most intuitive Kanban tool for beginners — its drag-and-drop interface is very fast to set up and the card model is flexible and visual. However, Trello has no native integration with code repositories, meaning there is always a disconnect between where the code lives (GitHub) and where the tasks are tracked (Trello). For a software development project, this separation creates overhead and risks the board falling out of sync with actual code changes.

Jira sits at the opposite end of the spectrum. It is the most powerful Agile project management tool in the market, with deep support for Scrum sprints, velocity tracking, burndown charts, and highly configurable workflows. However, this power comes with significant complexity — Jira has a steep learning curve and can feel bureaucratic for small or solo projects. For a student project, the setup cost is disproportionate to the benefit.

GitHub Projects occupies a useful middle ground. Its deepest strength is the native integration with GitHub Issues, Pull Requests, and branches — actions in the codebase automatically update the project board without any manual effort. This tight coupling means the board stays accurate almost for free. Its weakness is that it lacks the advanced sprint analytics (burndown charts, velocity trends) that Jira provides, and its automation capabilities, while improving with each GitHub release, are still less sophisticated than Jira's.

For the RPL project — a solo developer with a code-first workflow hosted entirely on GitHub — GitHub Projects with the Automated Kanban template is the right tool. It is not the most powerful option, but it is the most coherent one given the context.

**The WIP Limit Discipline**

Finally, implementing WIP limits revealed something about my own working habits that I had not fully appreciated before. Setting a maximum of 3 tasks in "In Progress" sounds simple, but when I populated the board with Sprint 1 tasks, my immediate instinct was to put five or six tasks into "In Progress" simultaneously. The WIP limit forced me to make an explicit choice about what the current priority actually is. This experience gave me a practical understanding of why Kanban's "stop starting, start finishing" principle exists — it is not a bureaucratic rule but a discipline that protects focus and ensures work actually reaches completion rather than accumulating indefinitely in an in-progress state.

---

*Reflection prepared for Assignment 7 — RPL Application System*
*Author: Boniface Kabaso | March 2026*
*(Word count: approximately 620 words)*
