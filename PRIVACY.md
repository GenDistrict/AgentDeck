# AgentDeck Privacy and Data Handling

Effective date: August 20, 2026

This policy describes data handling for the AgentDeck desktop application, paired AgentDeck PWA, device-pairing and encrypted-relay services, update services, and AgentDeck service accounts. These products and services are provided by **MAI DEPOT, Inc.** under the GenDistrict brand.

This is the product-specific policy for AgentDeck. The separate GenDistrict corporate-website policy does not replace this document.

## 1. Core privacy boundary

AgentDeck does not use its control-plane services to receive or centrally store your prompt and response bodies, reasoning content, tool or terminal output, work-file contents, local file and folder paths, environment variables, or model-provider credentials.

This does **not** mean that every AI request stays on your computer. When you choose a model provider, connector, gateway, or other external service, AgentDeck sends the information required for that request to the selected service. That service's data, retention, and model-training policies apply. If you require provider-side storage or training opt-out, you or your organization must select and configure the appropriate provider setting, plan, region, or contract. AgentDeck cannot do this on your behalf.

## 2. Information stored on your computer

Depending on the features you use, AgentDeck stores the following in the application's local user-data area or an account-specific configuration directory:

- AgentDeck account profiles and provider type;
- separate Claude and Codex configuration-directory references;
- registered workspaces and session metadata;
- session names, archive state, drafts, local usage records, and approval state;
- routines and recent execution results;
- paired-device identity, public-key fingerprints, token hashes, and capability settings;
- remote-access, notification, keep-awake, privacy, security, and update settings;
- startup and error logs; and
- optional dependencies managed by the application.

Provider credentials remain in the relevant account-specific configuration, OS credential store, cloud credential chain, or organization-managed secret system. AgentDeck diagnostics are designed not to read or include credential files.

## 3. Information processed by AgentDeck services

When cloud-connected features are enabled, AgentDeck may process:

- the AgentDeck service-account identifier used for authentication;
- registered-device identifiers, display information, public keys, token hashes, connection state, and last-seen time;
- application version, operating-system family, architecture, and update status;
- daily aggregated token counts, cache counts, and list-price usage estimates;
- allowlisted operational event codes, timestamps, counters, and success or failure state; and
- short-lived pairing, connection, and encrypted-relay metadata.

Operational events are limited to events such as application start, authentication, device connection, session state, and update success or failure. They are not intended to contain conversation or work-product content.

We use this information to authenticate users, pair and revoke devices, establish remote connections, provide update and status services, display usage, diagnose reliability and abuse, and protect the Service. AgentDeck does not sell this information or use conversation content for advertising.

## 4. Model providers, APIs, gateways, and connectors

Messages, selected context, attachments, or tool inputs are sent to a model provider only when required for the request you initiate or authorize. Connectors and external tools may send data to the service they connect to. Organization-managed deployments may route model requests through an approved gateway or infrastructure controlled by the organization.

Those third parties act under their own agreements and policies. Review their retention, training, region, access-control, and deletion settings before sending sensitive information. Disabling AgentDeck telemetry or deleting an AgentDeck service account does not delete data already submitted to a provider.

## 5. Local privacy and security features

When enabled, personal-data and sensitive-context protection can replace detected or user-defined information with pseudonyms before transmission and restore placeholders locally in the response. Detection rules and the masking dictionary remain on the computer. The pseudonym vault is encrypted with AES-256-GCM, is not exposed to agent tools, and is deleted with the session.

Prompt-injection protection can inspect attachments and content returned by tools, web sources, and connectors before model exposure. Learned approval history and automatic-review state remain local. These Beta protections can produce false positives or false negatives and do not replace human review or an organization's compliance controls.

## 6. Paired devices and encrypted relay

- First-time pairing requires explicit desktop approval and a matching short-lived safety code.
- Device identity is pinned using a P-256 public-key fingerprint. A changed identity requires re-pairing.
- Remote session frames are end-to-end encrypted using AES-256-GCM with keys derived through P-256 ECDH and HKDF-SHA-256.
- Fresh ephemeral session keys provide forward secrecy.
- Direct WebRTC connectivity is preferred. If a relay is required, it carries opaque encrypted frames and is not designed to persist or decrypt conversation content.
- Relay and connection infrastructure can observe limited metadata such as account/device association, connection timing, network addressing needed for delivery, and traffic volume.
- Pairing and relay tickets are short-lived. Per-device capabilities can be limited or revoked.

## 7. Diagnostics and support files

A diagnostic export may contain application, runtime, operating-system, CPU, memory, architecture, provider type, sign-in state, item counts, CLI availability, masked paths, and recent startup logs.

Diagnostics are designed to omit account names, email addresses, messages, prompts, reasoning, work-folder names, file contents, tokens, cookies, passwords, and provider credentials. Known user paths and secret-like values are masked before export. You must review a diagnostic file before choosing to send it to support.

Do not include credentials, private transcripts, source files, or unreviewed diagnostics in a public GitHub issue.

## 8. Retention

Unless a longer period is needed for security, legal obligations, or an active support request, AgentDeck uses the following default control-plane retention periods:

- raw operational events: 30 days;
- daily usage snapshots and administrative audit records: 400 days; and
- diagnostic files intentionally uploaded for support: 7 days.

Short-lived pairing and relay credentials expire after their immediate connection purpose. Local data remains until you remove it through the application, delete the application's data, or uninstall and choose data removal. Third-party providers apply their own retention periods.

## 9. Deletion and provider revocation

You can remove accounts, workspaces, sessions, routines, and paired devices in AgentDeck. Uninstalling may offer a choice to keep or remove local data; unattended removal can preserve data so a later installation can recover settings.

The **Delete AgentDeck service account** control removes the AgentDeck authentication user, registered devices, usage snapshots, and operational events after recent sign-in verification. It does not delete local projects and sessions or close Claude, OpenAI, cloud-provider, connector, or other third-party accounts.

To fully revoke a provider session or delete provider-held data, use that provider's security, privacy, or account-deletion controls separately.

## 10. Security

We use technical and organizational safeguards appropriate to the information processed, including encrypted transport, end-to-end encryption for remote session frames, hashed long-lived device tokens, device-key pinning, signed desktop releases, allowlisted remote methods, scoped capabilities, audit records, and access controls.

No system is completely secure. Protect the devices and accounts you pair, revoke lost or compromised devices promptly, and report suspected AgentDeck vulnerabilities according to [SECURITY.md](SECURITY.md).

## 11. International processing and your choices

AgentDeck infrastructure and service providers may process limited account, device, operational, and connection information in countries other than your own. Model providers, gateways, and connectors process submitted data in the regions and under the arrangements selected by you or your organization.

Depending on applicable law, you may have rights to request access, correction, deletion, or information about personal data handled by MAI DEPOT, Inc. You can exercise many deletion and revocation choices directly in AgentDeck. For another privacy request, contact us using the address below. We may need to verify your identity before completing a request.

## 12. Changes and contact

We may update this policy when the product or its data practices change. Material changes will receive a new effective date and may be shown in the application.

Privacy questions or requests: `contact@maidepot.com`

## 한국어 핵심 안내

- AgentDeck 제품 데이터의 처리 주체는 **MAI DEPOT, Inc.**이며 GenDistrict 브랜드로 서비스를 제공합니다.
- AgentDeck 제어 서버는 프롬프트·응답 본문, 사고 과정, 도구·터미널 출력, 작업 파일 내용과 경로, 환경 변수, 모델 제공자 자격 증명을 중앙 저장하지 않습니다.
- 선택한 모델 제공자·커넥터·게이트웨이에는 사용자가 요청하거나 승인한 데이터가 전송되며, 그 제공자의 저장·학습·보존 정책이 적용됩니다.
- 제공자 측 저장·학습 제외가 필요하면 사용자 또는 조직이 해당 제공자의 설정·플랜·리전·계약에서 직접 옵트아웃해야 합니다.
- AgentDeck 클라우드는 로그인 식별자, 등록 기기, 앱 버전, 연결 상태, 집계 사용량, 허용된 운영 이벤트와 단기 연결 메타데이터를 처리할 수 있습니다.
- 개인정보·민감 맥락 마스킹과 프롬프트 인젝션 검사는 로컬에서 동작하며, 마스킹 사전과 학습형 승인 기록도 PC에 남습니다. 이 Beta 기능은 모든 유출이나 탐지 실패를 막는 보장이 아닙니다.
- 페어링된 기기의 세션 프레임은 종단간 암호화됩니다. 중계 서버는 본문을 복호화·저장하도록 설계되지 않았지만 연결 시각과 트래픽 양 같은 제한된 메타데이터는 관찰할 수 있습니다.
- 앱에서 AgentDeck 서비스 계정을 삭제해도 로컬 프로젝트나 제3자 제공자에 이미 전달된 데이터·계정은 자동 삭제되지 않습니다.

This Korean section is a convenience summary. The English policy above is the controlling version unless applicable law requires otherwise.
