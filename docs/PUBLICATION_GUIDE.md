# Publication Guide

## Safe release model

Maintain two distinct things:

1. a private working vault containing real information; and
2. a separate public template or sanitized example containing placeholders only.

Do not make a filled vault public, then try to clean it in place. Do not assume a `.gitignore` rule protects material that was already tracked, copied into a document, embedded in an image, or committed to history.

## Before any public action

1. Read `docs/PRIVACY_CHECKLIST.md` and decide whether the target is a template-only release.
2. Review every tracked file and the Git history for personal, third-party, credential, operational, and local-environment information.
3. Replace real content with placeholders or remove it from the public copy. Keep unknown values unknown.
4. Verify active documentation links and that examples use only the repository's real template paths.
5. Only then create a public commit, push, release, archive, or share link under your own approval process.

This guide does not perform a privacy scan, scrub prior history, rotate exposed credentials, or grant authority to publish.

## What a public template may contain

- Markdown templates with generic placeholders
- Explanations of source-of-truth routing and privacy boundaries
- Example folder structure and fictional clearly-labelled examples
- License, security policy, and publication checklist

## What it must not contain

- A real filled vault or local copy of one
- Credentials, secrets, operational details, private contacts, or identifying data
- Raw exports, screenshots, chat transcripts, documents, or third-party confidential material
- Claims that an example has been deployed, accepted, or privacy-audited without direct evidence

## Suggested public description

```text
Local-first Markdown template for minimum-context AI handoff, source-of-truth routing, and privacy-safe personal workflow structure.
```
