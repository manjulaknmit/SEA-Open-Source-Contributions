# Open-Source Software Engineering: Contributing to a Library Management System

**Student Name:** ASHWIN BALUSU  
**USN:** NB25CSE360  
**Case Study:** 4 – Open-Source Software Engineering

---

## 1. Introduction

Open-source software is software whose source code is made available for people to use, study, modify, and distribute under the terms of an open-source licence. It is commonly developed through collaboration between developers and users in different locations.

Open-source software engineering applies software engineering practices—such as planning, coding, testing, documentation, version control, and review—to projects developed openly and collaboratively.

## 2. Case Study

This case study considers a student contributing documentation to an open-source **Library Management System**. Such a system may help a library maintain book records, manage member information, record book issues and returns, and track due dates.

A useful contribution does not have to involve writing program code. Clear documentation can help users understand how to install, configure, and use the software, and can help future contributors understand the project.

## 3. Objectives of the Contribution

- Understand the structure and contribution guidelines of an existing open-source project.
- Identify a documentation gap or an unclear explanation.
- Improve the relevant documentation without changing unrelated project files.
- Use Git and GitHub to track and propose the change.
- Learn how maintainers review and discuss community contributions.

## 4. Contribution Workflow

### Step 1: Select a repository

Choose a public repository for the Library Management System. Read its `README` file, licence, contribution guidelines, and code of conduct, if available. Check existing documentation and open issues to avoid duplicating another contributor's work.

### Step 2: Fork the repository

A fork is a personal copy of another user's repository on GitHub. Forking allows a contributor to make changes without needing direct write permission to the original project.

On GitHub, open the original repository and select **Fork**, then create the fork under your own account.

### Step 3: Clone the fork

Clone the fork to the local computer:

```bash
git clone https://github.com/<your-username>/<repository-name>.git
cd <repository-name>
```

Add the original repository as the `upstream` remote so that changes in the original project can be fetched later:

```bash
git remote add upstream https://github.com/<original-owner>/<repository-name>.git
```

### Step 4: Create a feature branch

Create a separate branch for the documentation update:

```bash
git switch -c docs/improve-library-guide
```

A separate branch keeps the contribution isolated and makes it easier to review.

### Step 5: Update the documentation

For this case study, the student reviews the user guide and improves a section explaining how to issue and return books. The documentation should use clear language and, where appropriate, explain:

- How to find a book record.
- How to select a library member.
- How to record a book issue.
- How to record a return.
- How to check a due date or an overdue item.

The contributor should verify each instruction against the actual application. If a feature cannot be verified, it should not be described as though it exists.

### Step 6: Review and commit the change

Inspect the changes before committing:

```bash
git status
git diff
```

Stage the documentation file and create a descriptive commit:

```bash
git add README.md
git commit -m "docs: improve library issue and return guide"
```

Use the actual path of the edited documentation file if it is not `README.md`.

### Step 7: Push the branch

Push the feature branch to the contributor's fork:

```bash
git push -u origin docs/improve-library-guide
```

### Step 8: Open a Pull Request

On GitHub, open the fork and select **Compare & pull request**. Set the original repository's target branch as the base and the fork's feature branch as the head. Describe what was changed and why.

A Pull Request (PR) is a proposal to merge changes from one branch or repository into another. It allows maintainers to inspect the diff, ask questions, suggest improvements, and run checks before accepting the contribution.

### Step 9: Respond to review

Read maintainer feedback carefully. Make requested corrections on the same feature branch, commit them, and push again. The Pull Request will update with the new commits. The contribution is complete only when the maintainers decide how to handle the PR; submitting a PR does not guarantee that it will be merged.

## 5. GitHub Contribution Workflow Diagram

```text
        Original open-source repository
                     |
                     v
               Fork repository
                     |
                     v
              Clone your fork
                     |
                     v
             Create feature branch
                     |
                     v
          Edit and review documentation
                     |
                     v
               Commit changes
                     |
                     v
             Push branch to fork
                     |
                     v
              Open Pull Request
                     |
                     v
             Maintainer review
                     |
             +-------+-------+
             |               |
          Changes          Approved
          requested           |
             |                v
             +----> Update   Merge (if accepted)
                    and push
```

## 6. Benefits of Open-Source Contributions

1. **Collaborative learning:** Contributors learn from maintainers and other developers.
2. **Improved documentation:** Clear instructions make software easier to install and use.
3. **Practical experience:** Contributors practise Git, GitHub, branching, commits, and code review.
4. **Quality improvement:** Review and discussion can identify unclear instructions, errors, and missing information.
5. **Community participation:** Contributors help maintain software that can benefit a wider group of users.
6. **Professional development:** Public contributions can demonstrate communication, teamwork, and technical skills.

## 7. Good Practices

- Read the project's licence and contribution guidelines before making changes.
- Keep each contribution focused and make small, understandable commits.
- Use clear branch names and descriptive commit messages.
- Check spelling, formatting, links, and commands in documentation.
- Do not claim that a feature or procedure exists unless it has been verified.
- Explain the purpose of the change in the Pull Request.
- Respond respectfully to review comments and update the contribution when appropriate.

## 8. Conclusion

Open-source software engineering enables people to improve software through transparent collaboration. This case study demonstrates that even a documentation contribution to a Library Management System can be valuable. By forking a repository, creating a branch, editing and reviewing documentation, committing changes, and submitting a Pull Request, a student gains practical experience with a widely used collaborative development workflow.

## 9. References

- Git documentation: https://git-scm.com/docs
- GitHub documentation – Fork a repository: https://docs.github.com/en/get-started/quickstart/fork-a-repo
- GitHub documentation – About pull requests: https://docs.github.com/en/pull-requests
- Open Source Initiative – The Open Source Definition: https://opensource.org/osd
