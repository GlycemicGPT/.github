<p align="center">
  <img src="https://raw.githubusercontent.com/GlycemicGPT/.github/main/assets/logo.png" alt="GlycemicGPT" width="160" height="160"/>
</p>

<h1 align="center">GlycemicGPT</h1>

<p align="center">
  <strong>Open source AI-powered diabetes management.</strong><br/>
  <em>Built by patients who got tired of waiting.</em>
</p>

<p align="center">
  <a href="https://glycemicgpt.org">Website</a> &middot;
  <a href="https://github.com/GlycemicGPT/GlycemicGPT">Platform</a> &middot;
  <a href="https://github.com/GlycemicGPT/GlycemicGPT/blob/develop/CONTRIBUTING.md">Contribute</a> &middot;
  <a href="https://github.com/GlycemicGPT/GlycemicGPT/discussions">Discussions</a>
</p>

---

### What is GlycemicGPT?

GlycemicGPT is a complete diabetes management platform that connects your CGM and insulin pump directly to an AI-powered analysis engine. Real-time monitoring, intelligent insights, caregiver alerting -- all self-hosted on your own infrastructure. No subscriptions. No vendor lock-in. Your data stays yours.

Think of it as what Nightscout, Loop, and an endocrinologist's pattern analysis would look like if they were built together from scratch with modern AI.

### What it does

**Data Aggregation & Monitoring**
- Real-time glucose trends from Dexcom G7 (cloud API) and Tandem pumps (direct BLE)
- Insulin-on-board tracking, basal rates, bolus history, reservoir levels
- Time in Range, CGM summary statistics, ambulatory glucose profile
- Web dashboard + Android app + Wear OS watch face

**AI-Powered Analysis**
- Daily briefs that analyze your overnight patterns, meal responses, and trends
- Multi-turn AI chat -- ask questions about your data like you would an endocrinologist
- RAG-powered research pipeline with clinical diabetes knowledge
- BYOAI: bring your own AI provider (Claude, OpenAI, Ollama, or any OpenAI-compatible endpoint)

**Alerting & Caregiver Ecosystem**
- Configurable glucose thresholds with predictive alerts
- Tiered delivery: in-app, push notification, Telegram, caregiver escalation
- Caregiver dashboard with read-only access and multi-patient support
- Watch alerts with dismiss-from-wrist capability

**Plugin Architecture**
- Extensible device support via capability-based plugins
- Tandem t:slim X2 and Mobi support built-in
- SDK for community-developed pump and CGM drivers
- Safety layer enforced at the platform level, not the plugin level

### Supported devices

| Device | Type | Connection | Status |
|--------|------|------------|--------|
| Dexcom G7 | CGM | Cloud API | Verified |
| Tandem t:slim X2 | Insulin Pump | BLE + Cloud API | Verified |
| Tandem Mobi | Insulin Pump | BLE + Cloud API | Protocol-compatible (untested on hardware) |

Support for additional pumps and CGMs is planned. The plugin architecture is designed for community contributions -- if you use a device we don't support yet, you can help add it.

### Architecture

| Component | Technology |
|-----------|------------|
| Backend API | FastAPI, Python 3.12, PostgreSQL, Redis |
| Web Dashboard | Next.js 15, React 19, Tailwind CSS, shadcn/ui |
| AI Sidecar | TypeScript, Express, multi-provider proxy |
| Android App | Kotlin, Jetpack Compose, BLE |
| Wear OS | Kotlin, Wear Compose, Watch Face Push API |
| Plugin SDK | Kotlin interfaces, capability-based, sandboxed |

Self-hosted via Docker Compose. One command to start everything:

```bash
git clone https://github.com/GlycemicGPT/GlycemicGPT.git
cd GlycemicGPT && cp .env.example .env
docker compose up --build -d
```

### Repositories

| Repo | Description | Status |
|------|-------------|--------|
| [**GlycemicGPT**](https://github.com/GlycemicGPT/GlycemicGPT) | Core platform: API, web dashboard, AI sidecar, mobile app, Wear OS, plugins | Active |

*Coming soon: `android-unofficial` (sideloaded builds), `android-playstore` (Play Store), `ios-unofficial`, `ios-appstore`, and `website` (glycemicgpt.org).*

### Key principles

- **Suggestions only** -- GlycemicGPT does not control medical devices
- **Self-hosted** -- your data stays on your infrastructure
- **BYOAI** -- bring your own AI provider, no forced subscriptions
- **Safety-first** -- pre-validation layer, emergency escalation, medical disclaimers
- **Open source** -- GPL-3.0, always free, community-driven

### Get involved

We welcome contributions from developers, designers, and people living with diabetes.

- Read the [Contributing Guide](https://github.com/GlycemicGPT/GlycemicGPT/blob/develop/CONTRIBUTING.md)
- Check out [Good First Issues](https://github.com/GlycemicGPT/GlycemicGPT/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22)
- Join the [Discussions](https://github.com/GlycemicGPT/GlycemicGPT/discussions)
- Read our [Governance](https://github.com/GlycemicGPT/GlycemicGPT/blob/develop/GOVERNANCE.md) to understand project roles

### Project roles

| Role | Description |
|------|-------------|
| **Contributor** | Anyone who opens issues, submits PRs, or joins discussions |
| **Committer** | Trusted contributors with write access to specific components |
| **Maintainer** | Project stewards responsible for releases, security, and direction |

See [GOVERNANCE.md](https://github.com/GlycemicGPT/GlycemicGPT/blob/develop/GOVERNANCE.md) for the path to growing your involvement.

---

> **Important: This software is not medical advice.**
>
> GlycemicGPT is experimental open-source software for educational and informational purposes only. It is not approved by the FDA or any regulatory body. AI can and will make mistakes -- hallucinate, misinterpret data, and provide outdated information. Do not replace professional medical care. Always verify suggestions with your healthcare team. See [MEDICAL-DISCLAIMER.md](https://github.com/GlycemicGPT/GlycemicGPT/blob/develop/MEDICAL-DISCLAIMER.md) for complete terms.
>
> **If you experience a diabetes emergency, contact your healthcare provider or emergency services immediately.**

---

<p align="center">
  <strong>Licensed under GPL-3.0</strong><br/>
  <sub>Built with care for the diabetes community.</sub>
</p>
