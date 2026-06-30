# Browser Agent Evaluation Checklist

Use this as a quick rubric for deciding whether a browser agent is demo-grade or production-grade.

## Scoring

Score every item as:

- `0` — not implemented, untested, or only works in a hand-crafted demo.
- `1` — implemented but brittle, partial, or missing durable receipts.
- `2` — implemented, exercised on a real site, and backed by repeatable proof.

Recommended gate:

- **Production-ready:** at least 80% of possible points, with no critical failures.
- **Demo-grade:** anything below that bar, or any workflow that depends on unverifiable claims.
- **Critical failure:** credential leakage, cookie/token exfiltration, destructive action without final-state proof, or reporting success from process exit alone.

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
