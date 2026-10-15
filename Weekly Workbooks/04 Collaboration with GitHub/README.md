# Collaboration with GitHub

You have been introduced to the personal git workflow (i.e., git add, git commit, git push etc.). The goal of today is to go through a full collaborative cycle.

# Tasks
### Task 1: Ensure you have completed the setup tasks from Week 2

This relates to setting up a GitHub project. You should view the project as a kanban board and be comfortable adding Issues to it (see [Task 5 from Week 2](../02%20Software%20Processes/README.md#task-5-set-up-your-kanban-board-and-add-your-first-issues)), and beginning to work on the README for your repository (see [Task 6 from Week 2](../02%20Software%20Processes/README.md#task-6-begin-writing-your-readme)). The full guidance on what to include in your README can be found [here](../../README%20requirements/README.md).

> [!TIP]
> Every time you see a task in the workbooks, add it as an issue in your Kanban board
> You can decide how to action it in the next team meeting, but this way you won't lose it. 


### Task 2: Set up `main` and `dev` branches

**Do this as a team**. Create a `dev` branch off `main`. On GitHub, use the branch dropdown, type `dev` and choose "Create branch: dev from main". Or from the command line (`git switch -c dev`). See [Git Flow and branching strategy](#git-flow-and-branching-strategy) in Further Reading for why we use this structure.

Once you have a `dev` branch, we'll set it to default next week. From then, the `dev` branch is what we'll be using to give you repo feedback. Ensure your `dev` branch is always up-to-date, and that it is **never** behind `main`!

The `main` branch will only continue to be the default branch for **this** workshop!

> [!WARNING]
> Work that is not on *dev* does not exist in the marking - we can only mark what we can see!

### Task 3: Set up your GitHub Project

Check that the Project (Kanban board) from Week 2 exists and is linked to your repository. It needs columns for at least `Todo`, `In Progress`, `In Review` and `Done`. Add an `In Review` column if you don't have one. The columns don't need to have these names exactly, and you can have additional columns if your team needs them!

### Task 4: Add three issues to the Kanban board

**As a team**, create three issues on your board:

- (a) Add an issue template
- (b) Add a pull request template
- (c) A third issue, depending on your repository (see paragraph below)

Prioritise (a) and (b). For teams that have already committed code, pick a small, real piece of work for (c), such as a bug or a small feature. For teams without code yet, work on your README for (c).

After this is done, split into pairs or threes and address **one issue each**. You will need to **assign yourselves to the issue** and move your card to `In Progress`.

### Task 5: Create a GitHub issue template

**This is done by the pair (or trio) working on issue (a)**

GitHub supports Markdown templates (with a YAML front matter block at the top giving the name, description and default labels) as well as YAML "issue forms" with proper input fields. See [Configuring issue templates for your repository](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository) and [Syntax for issue forms](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/syntax-for-issue-forms). Markdown templates are enough for this task, forms are optional but better.

1. Create a branch off `dev` named after your issue. A common convention is `type/issue-number-short-description`. Your team can pick its own, but write it down (see [Branch names](#branch-names)).

2. Create the issue template `.github/ISSUE_TEMPLATE/{...}.md`. You can create as many as you want. Common ones are `task.md`, `bug_report.md` and `feature_request.md`, but do what works for you as a team.

3. Commit in small steps. See [Commit messages](#commit-messages) in Further Reading.

4. Push your branch with `git push -u origin feature/{issue_number}-issue-template` once you are done.

5. Open a pull request:
   1. Click "Compare & pull request".
   2. **Set the base branch to `dev`, NOT `main`.** This is a very common mistake, so check the "base:" dropdown.
   3. Fill in the description (see [Pull requests](#pull-requests)), add `Closes #<issue_number>` (your issue number) and **assign reviewers**.
   4. Move your card to `In Review`.

> [!NOTE]
> You won't see your template in the "New issue" chooser yet, because GitHub only offers issue templates from the default branch (`main`). For now, check that the file renders correctly in your PR's "Files changed" tab. You will see it working after the release in Task 8.

### Task 6: Create a pull request template

**This is done by the pair (or trio) working on issue (b)**.

1. Create a branch off `dev` named after your issue, for example `feature/{issue_number}-pr-template`. Use your team's branch naming convention.

2. Create the pull request template `.github/pull_request_template.md`. GitHub pre-fills every new PR description with this file, so think about what a reviewer needs to see (see [Pull requests](#pull-requests) for writing good descriptions). Common sections are a summary, the related issue (`Closes #`), how to test, and a checklist. See [creating a pull request template](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/creating-a-pull-request-template-for-your-repository).

3. Commit in small steps: for example, one commit for the first draft of the template and another for the checklist. Write good commit messages (see Task 5 and [Commit messages](#commit-messages)).

4. Push your branch with `git push -u origin feature/{issue_number}-pr-template`.

5. Open a pull request, following the same steps as Task 5 step 5: **set the base branch to `dev`, NOT `main`**, add `Closes #<issue_number>`, assign reviewers and move your card to `In Review`.

### Task 7: Review the pull requests

Once the PRs are open, review each other's. For SEP-specific guidance on this see [Pull Requests and Code Review in SEP](code_review.md).

**Review it** (see [Code review](#code-review) in Further Reading). At least **two people who didn't write it** must review. Leave **inline comments**, then choose "Approve" or "Request changes". Try to label comments (see [Conventional Comments](https://conventionalcomments.org/)).

> [!TIP]
> You are **not** expected to review a PR that is too big - reject it and ask for smaller PRs (a rough guide is no more than 50-200 lines changed per PR, and ~2 open PRs per person per week). Agree in advance **who** will review and **by when**, and say no if the turnaround is unrealistic. Before a deadline, freeze `dev` at least 24 hours in advance.

**Authors:** respond to every comment by **pushing more commits to the same branch**. Don't open a new PR.

### Task 8: Merge

Once approved, merge into `dev` (see [Git Flow and branching strategy](#git-flow-and-branching-strategy) for how `dev` is later merged into `main`), resolving any conflicts which might occur. After the team has finished (a) and (b), take issue (c) through the same cycle: issue, branch, commits, PR into `dev`, two reviewers, merge.

**Release**

Once (a), (b) and (c) are merged into `dev`, release them to `main` via a `release` branch. Once you are done, create a new issue and a new PR to see your templates in use, close any leftover issues and move your cards to `Done`.

> [!TIP]
> **All real project work follows this cycle.** Your issues, commits and PRs are the evidence of your contribution. **Everyone should always have an issue in progress.**

# Further Reading

### Commit messages

Chris Beams' [How to Write a Git Commit Message](https://cbea.ms/git-commit/) is the de facto reference, setting out seven rules including imperative mood, a short subject line and a body that explains what and why. The [Pro Git book's section on contributing to a project](https://git-scm.com/book/en/v2/Distributed-Git-Contributing-to-a-Project) includes a concise set of commit guidelines. If you want structured messages that can drive automated changelogs and semantic versioning, the [Conventional Commits specification](https://www.conventionalcommits.org/) is worth a look, though it is a choice of structure rather than a standard for message quality.

### Branch names

There is no authoritative standard for branch names, and teams will generally settle on their own useful conventions. The only hard rules are the technical ones documented in [git check-ref-format](https://git-scm.com/docs/git-check-ref-format). A common pattern is `type/ticket-short-description` (for example `feature/PROJ-123-add-login`), but what matters most is that your team documents its convention and enforces it, ideally with a hook or CI check.

### Pull requests

Google's engineering practices include an excellent author's guide, with pages on [writing good change descriptions](https://google.github.io/eng-practices/review/developer/cl-descriptions.html) and [keeping changes small](https://google.github.io/eng-practices/review/developer/small-cls.html). They use the term "CL" (changelist), but the advice applies directly to pull requests. GitHub's own guide to [helping others review your changes](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/getting-started/helping-others-review-your-changes) is a practical, platform-specific complement.

### Code review

[Software Engineering at Google](https://abseil.io/resources/swe-book) is a strong choice here, and [Chapter 9 on code review](https://abseil.io/resources/swe-book/html/ch09.html) is free to read online. For something shorter and more actionable, the [reviewer's guide in Google's engineering practices](https://google.github.io/eng-practices/review/reviewer/) is excellent, starting with [The Standard of Code Review](https://google.github.io/eng-practices/review/reviewer/standard.html). [Conventional Comments](https://conventionalcomments.org/) is a lightweight convention for the tone and labelling of review comments, and the paper [Modern Code Review: A Case Study at Google](https://sback.it/publications/icse2018seip.pdf) provides the empirical backing. The SEP Knowledge Hub also has articles on [Code Reviews](https://github.com/spe-uob/knowledge-hub/blob/main/Code_Review.md) and [Writing code for others](https://github.com/spe-uob/knowledge-hub/blob/main/Writing_Code_For_Others.md).

### Git Flow and branching strategy

Vincent Driessen's blog post [A successful Git branching model](https://nvie.com/posts/a-successful-git-branching-model/) is a great place to start, but other good resources include Atlassian's [Gitflow Workflow tutorial](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow). Read the retrospective note at the top of Driessen's post: he says the model suits explicitly versioned software, not continuously delivered web apps. For simpler alternatives, see [GitHub Flow](https://docs.github.com/en/get-started/using-github/github-flow) and [trunkbaseddevelopment.com](https://trunkbaseddevelopment.com/), and DORA's page on [trunk-based development](https://dora.dev/capabilities/trunk-based-development/) summarises the research linking it to stronger delivery performance.








