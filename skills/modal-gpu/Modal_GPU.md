# Modal GPU

Use Modal only for the workload the user requested. Provider credentials, workspace configuration, source data, job logs, and remote resources are private.

- Confirm the workload, hardware, expected cost, and data destination when they are not explicit.
- Keep provider authentication in local configuration or a secret manager.
- Prefer the smallest suitable hardware and stop resources after the job completes.
- Report job outcomes and redacted diagnostics without exposing provider or data identifiers.
