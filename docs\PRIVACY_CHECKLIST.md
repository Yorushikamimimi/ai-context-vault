# Privacy Checklist

Use this before publishing a filled vault.

## Must Remove

- [ ] Real name, phone number, email, student ID, employee ID
- [ ] School, company, HR contact, interview link, meeting link if private
- [ ] Local absolute paths such as `C:\Users\...` or `/Users/...`
- [ ] Server IPs, domains, ports, usernames, passwords
- [ ] Tokens, API keys, cookies, OAuth credentials
- [ ] Raw exports such as `.xlsx`, `.csv`, `.pdf`, screenshots, chat logs
- [ ] Private notes from `40-Ops`, `60-Private`, and personal inboxes

## Should Replace With Placeholders

| Real Data | Placeholder |
|---|---|
| Your name | `{{NAME}}` |
| School | `{{SCHOOL}}` |
| Company | `{{COMPANY}}` |
| Interview time | `{{INTERVIEW_TIME}}` |
| Local vault path | `{{VAULT_PATH}}` |
| GitHub profile | `{{GITHUB_URL}}` |
| Email | `{{EMAIL}}` |

## Suggested Scan Terms

Search for:

```text
password
secret
token
api_key
phone
email
http
https
C:\
D:\
/Users/
@gmail
@qq
@163
```

