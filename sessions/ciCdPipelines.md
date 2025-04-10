# PowerShell in CI/CD Pipelines: A Practical Tour of Deployment Options

Speakers: Blake Cherry & Danny Stutz
Room: 404
Time: 11:10 - 11:55

## Session Description

Explore the diverse ways to deploy PowerShell scripts using DevOps continuous integration and continuous deployment (CI/CD) pipelines!

This session will investigate the options for running PowerShell in CI/CD processes. We'll start by discussing when and why you might want to incorporate PowerShell into your CI/CD pipelines, highlighting the benefits of automation, consistency, and efficiency in deployment workflows.

Next, we'll delve into various methods of deploying PowerShell within pipelines, including:
• Locally on Build Agents: Running scripts directly on the pipeline's host machine.
• Azure PowerShell DevOps Tasks: Utilizing built-in tasks for seamless integration with Azure services.
• Containers and Custom Dockerfiles: Exploring available PowerShell container images, considerations for modules requiring authentication, and best practices for creating custom Dockerfiles tailored to your needs.

We'll also compare the capabilities of different CI/CD platforms for running PowerShell, such as Azure DevOps, Jenkins, GitHub Actions, and GitLab. We'll discuss:

• Platform Differences: How each platform handles PowerShell execution via pipeline.
• Selection Criteria: Factors influencing the choice of platform for your specific use case.
• Advantages and Limitations: Understanding the strengths of each platform in the context of PowerShell deployment.

Additionally, we'll explore how PowerShell can be integrated with other DevOps tools like Terraform and Ansible, discussing key considerations and best practices for these scenarios.
By the end of this session, you'll have a comprehensive understanding of the options available for deploying PowerShell via pipelines and how to choose the best approach for your projects.

## Notes

- Code -> Version Control -> Automated Testing -> Controlled Deployment -> Consistent Results
  - Build out Pester testing on our CPE-MCM repositories
- CI/CD pipelines may allow dockerfiles to define an execution environment for ephemeral runners
- Security:
  - Verify agent Identity, ensure ACL scope
  - Secure Cloud - never hardcode, Use Svc Connections/oidc/managed ID
  - Protect Secrets via Vaults and mask in logging
  - Least Priv
