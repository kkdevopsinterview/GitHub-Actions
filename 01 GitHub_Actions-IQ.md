# 1. What is GitHub Actions?

**GitHub Actions** is a **CI/CD platform** built directly into
**GitHub** that allows automation of software workflows such as
**building**, **testing**, and **deploying applications**.

It allows developers to define **workflows using YAML files** that
automatically run when certain **events occur**, such as pushing code,
creating pull requests, or tagging releases.

Because it is integrated into GitHub, it eliminates the need for
separate **CI/CD tools** and simplifies **pipeline management**.

GitHub Actions supports automation for:

-   code build
-   testing
-   Docker image creation
-   deployment
-   infrastructure provisioning

It is widely used in **DevOps** for **continuous integration and
delivery**.

## Real-World Example

When a developer pushes code to the main branch, GitHub Actions
automatically runs tests and deploys the application.

## Interview Line

"GitHub Actions is an integrated CI/CD automation platform inside
GitHub."

------------------------------------------------------------------------

# 2. Why is GitHub Actions used in DevOps?

GitHub Actions is used because it automates repetitive **DevOps tasks**
such as testing, building, and deploying applications.

It improves:

-   speed of delivery
-   consistency
-   collaboration
-   automation

It allows pipelines to run automatically whenever **code changes**
occur, reducing manual work and errors.

It also integrates easily with **Docker**, **Kubernetes**, **cloud
platforms**, and **infrastructure tools**.

## Real-World Example

Automatically running unit tests and code quality checks on every pull
request.

## Interview Line

"GitHub Actions enables automated CI/CD workflows directly from GitHub."

------------------------------------------------------------------------

# 3. What is CI/CD and how does GitHub Actions support it?

**CI** stands for **Continuous Integration**, which means automatically
building and testing code whenever changes are made.

**CD** stands for **Continuous Delivery or Deployment**, which means
automatically deploying tested code to environments.

GitHub Actions supports CI/CD by:

-   triggering workflows on code changes
-   running automated tests
-   building Docker images
-   deploying to cloud or Kubernetes

It ensures **faster and safer software delivery**.

## Real-World Example

Pipeline that builds Docker image, pushes to registry, and deploys to
staging automatically.

## Interview Line

"GitHub Actions automates the CI/CD lifecycle from code commit to
deployment."

------------------------------------------------------------------------

# 4. What is a workflow in GitHub Actions?

A **workflow** is an automated process defined in a **YAML file** that
runs one or more jobs.

It is triggered by events such as:

-   push
-   pull request
-   release
-   manual trigger

Workflows define:

-   what triggers execution
-   what jobs should run
-   in what order

They are stored in a specific directory in the repository.

## Real-World Example

Workflow that runs tests on every pull request.

## Interview Line

"A workflow defines the automation pipeline in GitHub Actions."

------------------------------------------------------------------------

# 5. What is a runner?

A **runner** is a machine that executes the workflow jobs.

GitHub provides **hosted runners**, which are managed virtual machines.

Users can also configure **self-hosted runners** for custom
environments.

Runners execute:

-   scripts
-   Docker commands
-   deployment tasks

The runner environment determines available tools and operating system.

## Real-World Example

Ubuntu runner building a Node.js application.

## Interview Line

"A runner is the machine that executes workflow jobs."

------------------------------------------------------------------------

# 6. What are jobs in GitHub Actions?

A **job** is a group of steps that run on the same runner.

Jobs can run **sequentially or in parallel**.

Each job runs in a **fresh environment** unless dependencies are
defined.

Jobs allow structuring pipelines logically.

## Real-World Example

One job for testing, another for building, another for deployment.

## Interview Line

"A job is a collection of steps executed on a runner."

------------------------------------------------------------------------

# 7. What are steps in a job?

**Steps** are individual tasks inside a job.

Each step performs a specific action such as:

-   checking out code
-   installing dependencies
-   running tests
-   building Docker images

Steps execute sequentially inside a job.

They can run **shell commands** or **reusable actions**.

## Real-World Example

Step that installs dependencies before running tests.

## Interview Line

"Steps are individual tasks executed within a job."

------------------------------------------------------------------------

# 8. What is a trigger (event) in GitHub Actions?

A **trigger** defines when a workflow should run.

Common triggers include:

-   push to branch
-   pull request creation
-   release
-   manual dispatch

Triggers automate execution based on **repository events**.

Proper trigger configuration ensures pipelines run only when necessary.

## Real-World Example

Running CI pipeline only on changes to main branch.

## Interview Line

"A trigger defines when a workflow is executed."

------------------------------------------------------------------------

# 9. What is a YAML workflow file?

GitHub Actions workflows are written in **YAML format**.

The YAML file defines:

-   triggers
-   jobs
-   steps
-   environment variables

It describes the entire **automation pipeline declaratively**.

Using YAML makes workflows readable and **version-controlled**.

## Real-World Example

YAML file defining build and deployment process.

## Interview Line

"YAML workflow file defines automation steps declaratively."

------------------------------------------------------------------------

# 10. Where are GitHub Actions workflow files stored?

Workflow files are stored inside the repository under a specific
directory.

They are **version-controlled** along with application code.

Storing workflows in the repository ensures **transparency** and
**auditability**.

Changes to workflows follow the same Git process as code.

## Real-World Example

Developers updating pipeline through pull request.

## Interview Line

"Workflow files are stored inside the repository and
version-controlled."
