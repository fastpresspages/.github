<div align="center">

<img src="https://raw.githubusercontent.com/fastpresspages/.github/main/assets/banner.svg" alt="FastPress Labs — open-source launch tools for people who ship" width="100%">

# FastPress Labs

**Small, free, open-source tools for people who ship.**

[![LaunchGrade](https://img.shields.io/badge/launchgrade-v0.1.0-C6FF4A?labelColor=08080A)](https://github.com/fastpresspages/launchgrade)
[![CI](https://github.com/fastpresspages/launchgrade/actions/workflows/ci.yml/badge.svg)](https://github.com/fastpresspages/launchgrade/actions/workflows/ci.yml)
[![License](https://img.shields.io/badge/license-Apache--2.0-3DDC84?labelColor=08080A)](https://github.com/fastpresspages/launchgrade/blob/main/LICENSE)
[![Dependencies](https://img.shields.io/badge/dependencies-0-A78BFA?labelColor=08080A)](https://github.com/fastpresspages/launchgrade)

[Website](https://fastpresspages.github.io/launchgrade/) ·
[Free page audit](https://fastpresspages.github.io/launchgrade/#audit) ·
[LaunchGrade](https://github.com/fastpresspages/launchgrade) ·
[YouLauncher](https://fastpresspages.github.io/YouLauncher/) ·
[FastPress Start](https://fastpresspages.github.io/fastpress-start/) ·
[Hire page](https://fastpresspages.github.io/hire-me/) ·
[Email](mailto:meetcode99@gmail.com)

</div>

---

## Start here

```bash
npx -p github:fastpresspages/launchgrade launchgrade your.site
```

One command scans a public launch page across **53 checks in 7 categories** and tells you what to fix first. Takes about a minute. No account, no tracking, no paid API.

That is the whole pitch. The rest of this page is why it exists and how to work with us.

## Projects

| Project | What it is | Status |
| --- | --- | --- |
| **[LaunchGrade](https://github.com/fastpresspages/launchgrade)** | A zero-dependency launch-page grader: CLI, GitHub Action, MCP server and agent skill. Conversion, trust, technical, SEO, social, accessibility and AI-agent readiness. | **v0.1.0 · live** |
| **[YouLauncher](https://fastpresspages.github.io/YouLauncher/)** | A free one-page growth partner for people launching without a team. Built for the moment before you have a marketing department. | **live** |
| **[FastPress Start](https://github.com/fastpresspages/fastpress-start)** | A free, zero-build launch page template with SEO, privacy, accessibility, a working form and a public A+ audit. Fork it and ship in 15 minutes. | **live** |
| **[Hire page](https://fastpresspages.github.io/hire-me/)** | A zero-build, recruiter-friendly profile of verified work. Public code, dated reports, no invented experience. | **live** |

The real sample that keeps us honest: LaunchGrade's first scan of YouLauncher scored **[B- 71/100](https://github.com/fastpresspages/launchgrade/blob/main/samples/youlauncher-before/report.html)**. The fixes became the roadmap; the rebuilt page scored **[A+ 100/100](https://github.com/fastpresspages/launchgrade/blob/main/samples/youlauncher/report.html)**, with one deliberate warning (no analytics). We publish the before, not just the after.

## What we believe

- **Free beats gated.** A score you cannot see is not useful. The checklist, the weights and the reports are open.
- **Specific beats impressive.** "Add a privacy page" is a task. "Build trust" is a mood.
- **Agents are readers too.** Every product should explain itself to the models that will summarize it. `llms.txt`, `AGENTS.md` and MCP are part of the interface now.
- **No fake metrics. Ever.** No invented stars, users, revenue, logos, testimonials or partnerships. If it is on this page, it happened or it is clearly labeled as a plan.
- **Small tools, finished.** One useful tool beats five empty repositories.

## Built for humans and agents

- Product map for agents: [llms.txt](https://fastpresspages.github.io/launchgrade/llms.txt) · [full checklist](https://fastpresspages.github.io/launchgrade/llms-full.txt)
- Agent instructions: [AGENTS.md](https://fastpresspages.github.io/launchgrade/AGENTS.md)
- MCP server: `npx -y -p github:fastpresspages/launchgrade launchgrade-mcp`
- Installable skill: `npx skills add fastpresspages/launchgrade`

```json
{
  "mcpServers": {
    "launchgrade": {
      "command": "npx",
      "args": ["-y", "-p", "github:fastpresspages/launchgrade", "launchgrade-mcp"]
    }
  }
}
```

## Work with us

We are open to **collaborations, audits, sponsorships and paid builds** that fit the work. The bar is simple: useful to people who ship, honest about what it does, and free where it claims to be free.

- **Get a free human audit** of your launch page: [fastpresspages.github.io/launchgrade/#audit](https://fastpresspages.github.io/launchgrade/#audit)
- **Hiring Meet Shah:** [proof-of-work page](https://fastpresspages.github.io/hire-me/) with public code and dated reports
- **Propose a collaboration or a paid build:** [meetcode99@gmail.com](mailto:meetcode99@gmail.com) with what you ship and what you need.
- **Sponsor a check or a guide:** open an issue in [LaunchGrade](https://github.com/fastpresspages/launchgrade/issues) with the outcome you want.
- **Contribute:** start with [CONTRIBUTING.md](https://github.com/fastpresspages/.github/blob/main/CONTRIBUTING.md) and the [good-first-issue list](https://github.com/fastpresspages/launchgrade/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22).

We will not publish a partnership, customer count or endorsement we cannot show. That is not a limitation; it is the product.

## Community

- [Contributing](https://github.com/fastpresspages/.github/blob/main/CONTRIBUTING.md)
- [Code of Conduct](https://github.com/fastpresspages/.github/blob/main/CODE_OF_CONDUCT.md)
- [Security policy](https://github.com/fastpresspages/.github/blob/main/SECURITY.md)
- [Support](https://github.com/fastpresspages/.github/blob/main/SUPPORT.md)
- [Outreach field guide](https://github.com/fastpresspages/outreach) — goals, ideas and honest templates, in public
- [Press kit](https://github.com/fastpresspages/.github/blob/main/press.md) — boilerplate, facts, assets and coverage rules
- [Discussions](https://github.com/fastpresspages/launchgrade/discussions) — start with the [welcome post](https://github.com/fastpresspages/launchgrade/discussions/6)

<div align="center">
<br>
<sub>Apache-2.0 unless noted · Built in public by <a href="https://github.com/Meet6338-X">Meet Shah</a> · No fake metrics</sub>
</div>
