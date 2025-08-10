# Claude Code Instructions

This file contains mandatory instructions for Claude Code when working with this project.

## Development Practices

### Test-Driven Development (TDD)
- Always write tests first before implementing functionality
- Follow the Red-Green-Refactor cycle
- Ensure all new code has corresponding tests
- Run tests before and after making changes

### Security Best Practices
- Never commit secrets, API keys, or sensitive data to the repository
- Always use parameterized queries for database operations
- Validate and sanitize all user inputs
- Use secure authentication and authorization patterns
- Follow principle of least privilege for database access
- Implement proper error handling that doesn't expose sensitive information

### Directory Structure
- Follow language-specific best practices for project organization
- Maintain clear separation of concerns (models, views, controllers, services, etc.)
- Use consistent naming conventions throughout the codebase
- Organize tests to mirror the source code structure

### Pre-Commit Security Checks
- Always scan the codebase for secrets before committing changes
- Use tools like `git-secrets` or similar to detect accidentally committed credentials
- Review all changes for potential security vulnerabilities
- Ensure no hardcoded passwords, tokens, or API keys are present

### Environment and Configuration Management
- Always ensure `.gitignore` excludes `.env` files and other sensitive configuration
- Never commit environment files containing secrets
- Use environment variables for configuration that varies between deployments

### Application Configuration
- Write all application configuration in YAML format
- Encrypt all configuration files using SOPS with the GPG key: `13461447+carlosonunez@users.noreply.github.com`
- Store encrypted configuration files in the repository
- Decrypt configuration at runtime, never commit decrypted files

## Required Commands to Run

Before any commit:
1. Run all tests and ensure they pass
2. Run security scans for secrets
3. Verify `.gitignore` excludes `.env` files
4. Ensure all YAML configuration is SOPS-encrypted

## Project Context

This is the status-v3 project (renamed from status-setter).