# Security Integration

Your application’s repository typically includes source code, dependency configurations. By performing repository scanning, vulnerabilities across these components can be identified.

We utilize open-source tools to integrate security scanning into the workflow.

Repository scanning tools offer the following capabilities:
- **Static Application Security Testing (SAST)**: Examines the source code to uncover vulnerabilities.
- **Software Composition Analysis (SCA)**: Detects vulnerabilities in application dependencies and container images.

### Prepare Environment

In the CI pipeline, the analyzer scans, parses the results, and uploads them to the Code Secure Dashboard. An access token is required for authentication with the Code Secure Dashboard. The following are the required environment variables.

| ENV               | Require  | Description                                                                        |
|-------------------|----------|------------------------------------------------------------------------------------|
| CODE_SECURE_URL   | true     | The URL of code secure dashboard. Example: https://finding.example.com             |
| CODE_SECURE_TOKEN | true     | The CI Access Token used for authentication with the Code Secure Dashboard.        |
| GITLAB_TOKEN      | optional | The GitLab token used to comment on merge requests when new findings are detected. |

