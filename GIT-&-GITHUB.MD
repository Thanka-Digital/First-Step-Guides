# Git and Github workflow

When it comes to **Git & Github** we have some rules regarding the branches and commits that are created. Below is detailed breakdown of how we handle things at **Thanka**.

## Commit

For commit messages we encourage you to be more **atomic**, meaning commit as frequently as possible. _(Note: It doesn't mean you create commit message for each modification, rather write commit message for modifications that are related to each other)_.

Example:

```diff
project
  > auth
+    - login.auth.ts
+    - register.auth.ts
     - auth-config.ts
  > blog
+    - blog.create.ts
     - blog.read.ts
  - other-files
```

> For the example above write commit message for **login** and **register** in one message and seperate the **blog** modification to another commit message

---

The format in which commit messages should be written is like following.

`<tag>:<commit-message>`

For example:

- **feature: add login feature**
- **chore: created config file for eslint**
- **WIP: booking implementation** (WIP refers to **W**ork **I**n **P**rogress, sometimes you cannot finish some task for the day but we still encourage you to commit and push your code. So in order to warn fellow developers about the incomplete task use the **WIP** tag)

## Branching for private projects

**Branching** is handled in two different ways here at Thanka for private repos (client projects, inhouse projects, etc) and public repos (open source projects).

In this section we will talk about how to handle branching in private projects.

```
      hotfix/<issue-bug-name> (Quick fixes branch)
        |
main (production branch)
  |
  dev (development branch)
      |
    feat/<feature-name> (respective feature branches)

```

- **MAIN (Production)** branch is the branch where all the production ready codes will be merged for release or deployment.
  - Things to remember:
    - **DO NOT PUSH DIRECTLY TO MAIN**
    - **DO NOT SEND PR FROM ANY OTHER BRANCHES OTHER THAN DEV AND HOTFIX**
- **DEV (Development)** branch is the branch (sometimes also referred to stagging branch) where we will first merge all works/codes to before sending to `Main branch`.
  - Things to remember:
    - **TRY NOT TO PUSH DIRECTLY INTO DEV UNLESS NECESSARY**
    - **NO CREATION OF HOTFIX BRANCHES FROM DEV**
    - **SEND PR TO DEV FROM FEATURE BRANCHES**
- **Feature** branches are the branches you will be mostly working on. For each new feature/module you need to work you create new branch (using the convention of `feature/<feature-name>`) from **DEV** branch
  - Things to remember:
    - **AFTER COMPLETING YOUR TASK SEND PR TO DEV NOT MAIN**
    - **DO NOT DELETE THE BRANCH RIGHT AWAY EVEN AFTER SUCCESSFULL MERGES**
- **HOTFIX** branches are quick branches that will be exception when we need to quickly fix some issues in the `main branch`.
  - Things to remember:
    - **CREATE HOTFIX ONLY FROM MAIN WHEN NEEDED**
    - **SEND PR TO MAIN ON TASK COMPLETION**
    - **DELETE THE BRANCH WHEN PR MERGED**

## Branching for open source projects

In this section we will talk about how to handle branching in public projects.

```
      hotfix/<issue-bug-name> (Quick fixes branch)
        |
release (release branches)
  |
  dev (development branch)
      |
    feat/<feature-name> (respective feature branches)

```

As you can see the branching system is similar to private one except for few changes. Let's address the elephants in the branch.

- **RELEASE** branch are branches created to deploy major version release **_(example: v1.3, v2.78, etc)_**
  - Things to remember:
    - **DO NOT PUSH DIRECTLY TO RELEASE BRANCHES**
    - **ONLY MERGE PR FROM DEV AND HOTFIX**
    - There will be multiple release branches related to each major release and its corresponding minor + patch releases. The onces that will get deleted are the one that are depricated and not supported anymore.
- **FEATURE** branch are similar to the private project only you have to **CREATE THEM IN YOUR OWN `FORKED REPO` AND NOT IN THE `MAIN REPO`**
