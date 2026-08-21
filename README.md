# AgentDeck

AgentDeck is a desktop control center for running and supervising Claude and Codex sessions from one workspace. It supports multiple accounts, isolated sessions, approvals, remote PWA access, routines, usage visibility, and signed desktop updates.

This repository is the official public distribution and support page for AgentDeck. The application source code and release-signing infrastructure are maintained privately.

## Download

Current stable release: **0.1.170**

| Platform | Download | Requirements |
| --- | --- | --- |
| Windows | [AgentDeck Setup 0.1.170.exe](https://storage.googleapis.com/gendistrict-agentdeck-updates/releases/0.1.170/windows/x64/AgentDeck%20Setup%200.1.170.exe) | Windows 10/11, x64 |
| macOS | [AgentDeck-0.1.170-arm64.dmg](https://storage.googleapis.com/gendistrict-agentdeck-updates/releases/0.1.170/macos/arm64/AgentDeck-0.1.170-arm64.dmg) | macOS 13+, Apple Silicon |
| Web | [Open AgentDeck PWA](https://agentdeck.gendistrict.com) | A paired AgentDeck desktop |

The desktop downloads above use immutable, version-specific URLs. Checksums are published in [SHA512SUMS.txt](SHA512SUMS.txt).

## Verify the installers

- Windows installers are Authenticode-signed by `MAI DEPOT, Inc`.
- macOS installers are signed with Developer ID Application `MAIDEPOT, Inc (WAH9N3NJX5)`, notarized by Apple, and stapled.
- Compare the downloaded file with [SHA512SUMS.txt](SHA512SUMS.txt) before installation when independent verification is required.

## Accounts and third-party services

AgentDeck does not provide Claude, ChatGPT, Codex, API, or connector subscriptions. Users are responsible for their accounts, provider terms, and usage charges.

## Support

- For ordinary bugs and feature requests, use this repository's Issues page.
- Do not attach access tokens, credentials, private conversation transcripts, source files, or unreviewed diagnostic files.
- For security issues, follow [SECURITY.md](SECURITY.md) and report privately.

## Legal

AgentDeck is proprietary software distributed by Gen District. No open-source license is granted by this repository. See [TERMS.md](TERMS.md), [PRIVACY.md](PRIVACY.md), and [NOTICE.md](NOTICE.md).

Copyright © MAI DEPOT, Inc. All rights reserved.
