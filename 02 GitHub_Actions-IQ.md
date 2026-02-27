# 11. What are self-hosted runners?

**Self-hosted runners** are machines that you manage yourself to run
**GitHub Actions workflows**. Instead of using GitHub's managed virtual
machines, you install a **runner agent** on your own server, VM, or even
on-premises machine.

Self-hosted runners are useful when:

-   you need custom software or tools
-   you require access to internal networks
-   you need better performance
-   you want cost optimization

They provide more flexibility but require **maintenance and security
management**.

Unlike GitHub-hosted runners, self-hosted runners **persist between
jobs** unless cleaned manually.

## Real-World Example

Using a self-hosted runner inside a private network to deploy to an
internal Kubernetes cluster.

## Interview Line

"Self-hosted runners provide custom execution environments managed by
the organization."

------------------------------------------------------------------------

# 12. What is the difference between GitHub-hosted and self-hosted runners?

**GitHub-hosted runners** are managed by GitHub. They provide **fresh
virtual machines** for each job and come pre-installed with common
tools. They are easy to use and require no maintenance.

**Self-hosted runners** are managed by the user. They offer full control
over environment configuration but require **maintenance, security
management, and updates**.

GitHub-hosted runners are ideal for most standard CI tasks.\
Self-hosted runners are better for specialized workloads or internal
deployments.

Choosing between them depends on **cost, control, and infrastructure
needs**.

## Real-World Example

Using GitHub-hosted runners for testing and self-hosted runners for
production deployments.

## Interview Line

"GitHub-hosted runners are managed; self-hosted runners provide full
control."

------------------------------------------------------------------------

# 13. How do you pass environment variables in GitHub Actions?

**Environment variables** can be defined at different levels in a
workflow:

-   workflow level
-   job level
-   step level

They are used to pass configuration values such as **API URLs,
environment names, or credentials**.

Environment variables improve flexibility and prevent **hardcoding
values**.

Variables can also be dynamically generated during workflow execution.

Managing environment variables properly ensures clean and maintainable
pipelines.

## Real-World Example

Passing environment variable to select deployment environment (dev or
prod).

## Interview Line

"Environment variables allow dynamic configuration inside workflows."

------------------------------------------------------------------------

# 14. What are secrets in GitHub Actions?

**Secrets** are encrypted values stored securely in GitHub repositories
or organization settings.

They are used to store sensitive information such as:

-   API keys
-   cloud credentials
-   tokens
-   passwords

Secrets are injected into workflows securely and are not exposed in
logs.

Proper secret management prevents accidental leaks.

Secrets are essential for secure CI/CD pipelines.

## Real-World Example

Using cloud access keys stored as repository secrets for deployment.

## Interview Line

"Secrets securely store sensitive data for CI/CD workflows."

------------------------------------------------------------------------

# 15. How do you secure secrets in workflows?

Secrets should never be **hardcoded** in workflow files.

They must be stored in **GitHub Secrets** and referenced securely.

Best practices include:

-   limiting secret access
-   rotating credentials regularly
-   avoiding printing secrets in logs
-   using environment protection rules

Also, secrets should only be used in necessary jobs to minimize
exposure.

Security in CI/CD is critical because pipelines often have access to
production systems.

## Real-World Example

Using separate secrets for staging and production environments.

## Interview Line

"Secrets must be encrypted, scoped, and never hardcoded."

------------------------------------------------------------------------

# 16. What is matrix strategy?

**Matrix strategy** allows running the same job across multiple
configurations in parallel.

For example, you can test an application across different:

-   operating systems
-   language versions
-   environments

Matrix builds reduce duplication in workflow definitions and increase
test coverage.

It improves automation efficiency and ensures compatibility across
environments.

## Real-World Example

Testing a Node.js application across multiple Node versions.

## Interview Line

"Matrix strategy enables parallel execution across multiple
configurations."

------------------------------------------------------------------------

# 17. How do you cache dependencies in GitHub Actions?

**Caching** stores dependencies between workflow runs to speed up
execution.

Without caching, dependencies must be downloaded every time, increasing
build time.

GitHub Actions provides built-in **caching mechanisms**.

Proper cache keys ensure correct reuse and invalidation when
dependencies change.

Caching significantly improves CI performance.

## Real-World Example

Caching npm or Maven dependencies to reduce build time.

## Interview Line

"Caching improves pipeline speed by reusing dependencies."

------------------------------------------------------------------------

# 18. What is artifact storage?

**Artifacts** are files generated during workflow execution that can be
stored and accessed later.

Examples include:

-   build outputs
-   test reports
-   Docker images
-   compiled binaries

Artifacts help in debugging and multi-stage pipelines.

They can be downloaded from GitHub UI or used in subsequent jobs.

Artifact management improves traceability.

## Real-World Example

Storing build artifacts for later deployment.

## Interview Line

"Artifacts preserve workflow outputs for reuse and debugging."

------------------------------------------------------------------------

# 19. How do you deploy applications using GitHub Actions?

## Interview Explanation

Deployment in GitHub Actions is usually implemented as a job that runs
after successful build and test stages.

It may include:

-   building Docker image
-   pushing image to registry
-   applying Kubernetes manifests
-   triggering Argo CD

Deployment steps use secrets for authentication.

Conditional logic ensures deployment runs only on specific branches.

Automation ensures consistent and repeatable releases.

## Real-World Example

Deploying application to staging after merging into main branch.

## Interview Line

"Deployment jobs automate application release after successful CI."

------------------------------------------------------------------------

# 20. How do you integrate GitHub Actions with Docker?

GitHub Actions integrates easily with **Docker**.

Common workflow includes:

-   building Docker image
-   tagging image
-   pushing to container registry

Docker commands run inside workflow steps.

Docker build and push operations are automated within CI pipeline.

This ensures containerized deployments remain consistent.

## Real-World Example

Building Docker image on every push and pushing to Docker Hub or AWS
ECR.

## Interview Line

"GitHub Actions automates Docker build and registry push processes."
