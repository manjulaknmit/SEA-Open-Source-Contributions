# Open-Source Software Engineering: Improving Library Management System Documentation

## Student Details
- **Name:** YERRAKONDAPPAGARI JEEVANA San
- **USN:** NB25CSE417
- **Section:** F
- **Assigned Case Study:** Question 4 – Open-Source Software Engineering

## 1. Introduction

Open-source software is software whose source code is available for people to view, use, modify, and improve according to its licence. It is usually developed through collaboration, where contributors work on different parts of the same project.

GitHub makes this collaboration easier by providing tools such as repositories, forks, commits, issues, and pull requests. A contributor does not need to be the owner of a project to suggest an improvement.

In this case study, a Library Management System is already hosted on GitHub. The project does not clearly explain how users can issue and return books. I will contribute by preparing simple documentation that explains these two operations.

## 2. Problem Analysis

A Library Management System may have working features, but users can still find it difficult to use when instructions are missing.

For example, a student may not know how to request a book, and a librarian may be unsure about the steps to record a return. This can lead to confusion, incorrect entries, and repeated questions.

The main problem is therefore not necessarily a software bug. It is a documentation gap. The project needs clear, step-by-step instructions for issuing and returning books.

## 3. Proposed Solution

I would add a Markdown documentation file, such as `docs/book-issue-and-return.md`, to the project. It would explain the process in everyday language.

### 3.1 Book issuing process

1. The librarian signs in to the Library Management System.
2. The librarian searches for the required book using its title, author, or book ID.
3. The system displays the book details and its availability.
4. The librarian checks that the student has a valid library account and has not crossed the borrowing limit.
5. The librarian selects the student and confirms the issue.
6. The system records the issue date and expected return date.
7. The book status is updated to **Issued**, and the student is informed of the due date.

### 3.2 Book returning process

1. The librarian opens the return-book section.
2. The librarian searches for the issued book using the book ID or the student's details.
3. The system displays the issue record and due date.
4. The librarian checks the returned book and records its condition.
5. The librarian confirms the return.
6. The system updates the book status to **Available**.
7. If the book is returned late, the system calculates or displays the applicable fine according to the library rules.

*Note: These steps describe a proposed user guide. The exact buttons, fields, borrowing limits, and fine rules should be adjusted to match the actual application.*

### 3.3 Example

Suppose a student named Ananya wants to borrow a book called *Introduction to Java Programming*.

- The librarian searches for the book and confirms that it is available.
- The librarian selects Ananya's library account and records the issue.
- The system saves the issue date and due date.
- A week later, Ananya returns the book.
- The librarian finds the issue record and confirms the return.
- The book becomes available for the next student.

This example helps a new user understand the complete process without needing technical knowledge.

## 4. GitHub Workflow for the Documentation Contribution

I would follow the normal open-source contribution process so that the project owner can review the change before it is added to the original repository.

### Step 1: Open the original repository

Visit the Library Management System repository on GitHub and read its README file, contribution guidelines, and existing documentation. This helps me understand the project's structure and avoid duplicating an existing guide.

### Step 2: Fork the repository

Click **Fork** to create a copy of the original repository under my own GitHub account. I can make changes in this copy without directly changing the owner's project.

### Step 3: Create or update the documentation file

Open the forked repository and create the file `docs/book-issue-and-return.md` (or use the documentation folder already followed by the project). Add the issue and return instructions, an example, and any relevant notes.

### Step 4: Commit the changes

After checking the spelling, links, and Markdown formatting, save the file with a clear commit message, for example:

`Added book issue and return documentation`

A commit records the change and makes it easier for the maintainers to understand what was updated.

### Step 5: Submit a Pull Request

Open the **Pull requests** tab and select **New pull request**. Compare my fork's branch with the original repository's target branch. Add a meaningful title, such as:

`Add documentation for issuing and returning library books`

In the description, explain that the contribution adds user-friendly steps for issuing and returning books. Then submit the Pull Request.

### Step 6: Review and merge

The project maintainer checks the proposed documentation. They may suggest corrections or ask for changes. I can update my fork and push another commit to the same branch; the Pull Request will update automatically. Once the maintainer is satisfied, they can merge it into the original repository.

## 5. GitHub Contribution Workflow Diagram

```text
Original Library Management System Repository
                    |
                    v
              Fork Repository
                    |
                    v
       Create / Edit Documentation File
                    |
                    v
             Commit Changes
                    |
                    v
             Open Pull Request
                    |
                    v
          Maintainer Reviews Changes
                    |
             +------+------+
             |             |
        Changes needed   Approved
             |             |
             v             v
       Make updates      Merge PR
             |             |
             +----->-------+
                           |
                           v
             Documentation Updated
             in Original Repository
```

## 6. Benefits and Challenges

### Benefits of contributing to open source

1. **Better user experience:** Clear instructions help students and librarians use the system correctly.
2. **Shared improvement:** The documentation becomes available to everyone using the project, not just one person.
3. **Learning opportunity:** Contributors gain practical experience with GitHub, Markdown, version control, code review, and teamwork.
4. **Quality and consistency:** Maintainers can review proposed changes before they become part of the main project.

### Possible challenges

1. **Understanding the existing project:** The contributor must read the application and its current documentation so the instructions match the actual features.
2. **Review feedback:** The maintainer may request corrections or changes. The contributor should respond and update the Pull Request.

## 7. Conclusion

This case study shows that open-source contribution is not limited to writing program code. Improving documentation is also valuable because users need to understand how to work with the software.

By adding a clear guide for issuing and returning books and submitting it through a Pull Request, a student can help make the Library Management System easier to use. The fork, commit, review, and merge process also provides practical experience in collaborative software development.

---
**Contribution file:** `USN_Open_Source_Contribution.md`
