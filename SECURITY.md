# Security Policy

## Sensitive Data

This template is designed to store personal context. If you use it with real data, it may contain sensitive information.

Do not commit:

- passwords, tokens, API keys, SSH keys
- phone numbers, emails, HR contacts, interview links
- server IPs, domains, deployment credentials
- private diary, finance, relationship notes
- raw exports from Feishu, Notion, Google Drive, or other tools
- local absolute paths that reveal your machine structure

## Before Publishing

Run a manual review and follow `docs/PRIVACY_CHECKLIST.md`.

If sensitive data was committed, rotate the exposed credentials and remove the data from git history before publishing.

