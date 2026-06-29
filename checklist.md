# Browser Agent Evaluation Checklist

Use this as a quick rubric for deciding whether a browser agent is demo-grade or production-grade.

## Authentication

- [ ] Can reuse an existing browser profile without re-login.
- [ ] Can detect sign-in redirects and fail closed.
- [ ] Can hand off MFA/CAPTCHA/passkeys to a human without exposing secrets.
- [ ] Does not store credentials in scripts, skills, or logs.

## DOM complexity

- [ ] Handles iframe switching.
- [ ] Handles Shadow DOM roots.
- [ ] Handles hidden or responsive controls.
- [ ] Handles rich-text editors such as ProseMirror and Quill.
- [ ] Handles native browser dialogs separately from DOM dialogs.

## Reliability

- [ ] Uses stable selectors where possible.
- [ ] Verifies visible state after each destructive action.
- [ ] Retries transient navigation/render failures.
- [ ] Records screenshots or DOM snapshots for failures.

## Final-state proof

- [ ] Checks public URLs after publishing.
- [ ] Records object IDs, commit SHAs, receipt URLs, or final status text.
- [ ] Treats ambiguous states as unverified instead of success.
- [ ] Does not report success from process exit alone.

## Security

- [ ] Keeps browser profiles isolated by platform.
- [ ] Does not exfiltrate cookies/tokens.
- [ ] Avoids over-broad process kills.
- [ ] Uses proxy/direct routing intentionally and documents why.
