# Privacy Checklist for Public Release

Use this before publishing, sharing, opening a pull request, uploading an archive, or creating a public link for a vault-derived repository.

> A filled personal vault is not directly publishable. Create a separate sanitized copy, then review both its tracked files and its Git history.

## Stop conditions

Do not publish until every applicable item below is resolved. Removing a line from the latest working tree is not enough if the data remains in history, attachments, generated files, screenshots, or release assets.

## Remove or keep private

- [ ] Real names, usernames, personal email addresses, phone numbers, birth dates, student or employee identifiers
- [ ] Exact school, employer, client, recruiter, colleague, interview, meeting, calendar, or application details when they identify a person or private process
- [ ] Home, office, server, local absolute paths, hostnames, domains, IP addresses, ports, and infrastructure diagrams
- [ ] Passwords, tokens, API keys, cookies, OAuth credentials, SSH keys, recovery codes, and secret-bearing configuration files
- [ ] Private health, finance, diary, relationship, therapy, or personally identifying notes
- [ ] Raw chat exports, screenshots, audio, documents, spreadsheets, browser exports, issue exports, and third-party confidential text
- [ ] Git remotes, commit messages, history, branches, releases, and attachments that still contain any of the above

## Replace safely

| Sensitive or real value | Use instead |
|---|---|
| Person or organization | `{{PERSON}}`, `{{ORGANIZATION}}`, or a fictional clearly-labelled example |
| Date, location, contact, or identifier | `{{DATE}}`, `{{LOCATION}}`, `{{CONTACT}}`, `{{ID}}` |
| Local path or host | `{{VAULT_PATH}}`, `{{HOST}}`, `{{PORT}}` |
| Unsupported claim | `{{UNKNOWN}}` or an explicit `not verified` note |

Do not replace a missing fact with a realistic-looking fake fact that readers could mistake for real evidence.

## Review the publication surface

- [ ] Inspect every tracked file, including dotfiles, documentation, templates, sample data, and generated artifacts.
- [ ] Inspect staged and unstaged changes, Git history, branches, tags, release assets, and configured remotes.
- [ ] Check filenames, links, image metadata, document metadata, and copied command output for identifiers or local paths.
- [ ] Confirm ignored/private folders and credential files were neither added nor included indirectly.
- [ ] Ask an appropriate reviewer to check ambiguous material before release.

## Search aids, not proof

Focused searches can help find obvious terms such as `password`, `secret`, `token`, `api_key`, local home paths, personal email domains, or phone-like numbers. They do not prove a repository is safe: review context, encoded values, file metadata, generated assets, and history separately.
