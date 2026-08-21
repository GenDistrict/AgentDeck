# AgentDeck Security Policy

## Supported releases

Security fixes are provided for:

| Product | Supported version |
| --- | --- |
| AgentDeck desktop | Current stable release only |
| AgentDeck PWA and connection services | Currently deployed production version |

Older desktop versions should be updated when a signed stable update is available.

## Report a vulnerability privately

**Do not open a public GitHub issue for a suspected vulnerability.** Use one of these private channels:

1. [Open a private GitHub security advisory](https://github.com/GenDistrict/AgentDeck/security/advisories/new) (preferred).
2. Email `contact@maidepot.com` with the subject `AgentDeck security report`.

If sensitive evidence is required, first ask for a protected transfer method. Do not send passwords, access tokens, provider credentials, private conversation content, customer data, proprietary source code, or unreviewed diagnostic archives by ordinary email.

If a credential or paired device may already be compromised, revoke it with the relevant provider or in AgentDeck immediately; do not wait for our response.

## What to include

Provide the minimum information needed to investigate:

- affected AgentDeck version and operating system;
- affected component, such as desktop, PWA, pairing, encrypted relay, updater, account isolation, approvals, or a provider integration;
- reproducible steps or a minimal proof of concept using non-sensitive test data;
- expected security boundary and observed result;
- practical impact and required attacker access; and
- whether the issue is already public or actively exploited.

## Response and coordinated disclosure

We aim to acknowledge actionable reports within three business days. Investigation and remediation time depend on severity and reproducibility. Please allow time for a coordinated fix and signed release before public disclosure. We will provide status updates when there is material progress.

Submitting a report does not create a promise of payment or a bug bounty. Any reward program will be announced separately.

## Product security scope

Examples within scope include vulnerabilities in:

- AgentDeck account isolation and local credential boundaries;
- desktop IPC, file access, tool approvals, or remote-method authorization;
- PWA device pairing, identity pinning, revocation, end-to-end encryption, or relay authorization;
- signed update and release verification;
- local masking, prompt-injection review, or automation controls when a bypass crosses a documented security boundary; and
- AgentDeck-operated authentication, device, usage, or operational services.

Third-party model providers, cloud platforms, connectors, and user-operated gateways have their own security programs. Report a third-party vulnerability to that provider unless the issue is caused by AgentDeck's integration or exposes AgentDeck users across an AgentDeck boundary.

Reports based only on automated scanner output, denial-of-service traffic, social engineering, unsupported versions, or a device already controlled with equivalent administrator access may be closed unless they demonstrate a distinct AgentDeck vulnerability.

## Data handling boundary

AgentDeck does not issue Claude, ChatGPT, Codex, model-API, cloud, or connector credentials. Provider-side account compromise must also be revoked and reported through that provider. See [PRIVACY.md](PRIVACY.md) for the AgentDeck data boundary and retention policy.
