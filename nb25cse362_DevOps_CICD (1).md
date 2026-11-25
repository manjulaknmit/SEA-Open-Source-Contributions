# Question 3: DevOps Practices and CI/CD Pipelines

## Case Study: Online Shopping Application

**Name:** Sriniketan
**USN:** NB25CSE362  
**Subject:** Software Engineering and Applications (Unit V)  
**Assigned Case Study:** Question 3 – DevOps Practices and CI/CD Pipelines  


### 1. Introduction

DevOps is a software engineering approach that brings development and
operations teams together. Its main purpose is to improve collaboration,
automate repetitive tasks, and deliver software faster and more
reliably.

Continuous Integration (CI) is the practice of frequently combining code
changes into a shared repository and automatically building and testing
them. Continuous Delivery means keeping the application ready for
release, while Continuous Deployment automatically releases changes that
pass the required checks.

### 2. Problem Analysis

The software company develops an online shopping application. Developers
frequently add new features and fix bugs. However, manual testing and
deployment are causing delays and errors.

Manual processes can take a lot of time and may lead to mistakes. When
different developers work on the same application, their changes must
also be integrated and tested carefully.

### 3. Proposed Solution

The company can use DevOps practices and a CI/CD pipeline to automate
the process of building, testing, and deploying the application.

The developers can store their source code in a shared version-control
repository. Whenever a developer commits or pushes code, the CI/CD
pipeline can automatically start the required stages.

### 4. CI/CD Pipeline Stages

1.  **Plan:** The team identifies requirements, tasks, and improvements
    for the application.
2.  **Code:** Developers write code and make changes to the shopping
    application.
3.  **Build:** The system automatically compiles or packages the
    application and checks for build errors.
4.  **Test:** Automated tests check whether the application works
    correctly and whether new changes have caused problems.
5.  **Release:** A tested version is prepared for release.
6.  **Deploy:** The application is delivered to the production
    environment. In continuous delivery, release may require approval;
    in continuous deployment, successful changes are released
    automatically.
7.  **Monitor:** The team observes application performance, errors, and
    user experience.

### 5. Explanation of Build, Test and Deployment

-   **Build:** Converts the source code into a runnable or deployable
    application package. It helps identify compilation and packaging
    errors.
-   **Test:** Runs automated tests to check features such as login,
    product search, cart operations, and payment processing.
-   **Deployment:** Moves the approved application version to the server
    or cloud environment so that users can access it.

### 6. Benefits of Automation

1.  **Faster Delivery:** Automated building, testing, and deployment
    reduce the time needed to release new features.
2.  **Fewer Manual Errors:** Automation reduces mistakes that may occur
    during repetitive manual tasks.
3.  **Improved Software Quality:** Frequent testing helps identify bugs
    earlier and makes the application more reliable.
4.  **Better Collaboration:** Developers and operations teams can work
    together using a common process.
5.  **Faster Feedback:** Developers receive test and build results
    quickly after submitting code changes.

### 7. CI/CD Pipeline Diagram

``` mermaid
flowchart LR
    A[Plan] --> B[Code]
    B --> C[Commit to Repository]
    C --> D[Build]
    D --> E[Automated Testing]
    E --> F[Release]
    F --> G[Deploy]
    G --> H[Monitor]
    H -. Feedback .-> A
```

### 8. Conclusion

DevOps and CI/CD practices can help the company improve the development
and deployment of its online shopping application. Automation makes the
process faster, reduces manual errors, and improves software quality.
Regular monitoring and feedback also help the team identify and solve
problems quickly.
