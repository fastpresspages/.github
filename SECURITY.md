# Security policy

## Report a vulnerability

**Do not open a public issue for a security problem.**

Use GitHub's private vulnerability reporting on the affected repository:

- [LaunchGrade security advisories](https://github.com/fastpresspages/launchgrade/security/advisories/new)
- For anything that affects the organization or a repository without advisories enabled, email [meetcode99@gmail.com](mailto:meetcode99@gmail.com) with the subject `SECURITY`.

Include:

- the repository and version or commit
- what an attacker can do
- the smallest reproduction you can share
- any suggested fix or mitigation

You will get an acknowledgement when the report is read. There is no bug bounty and no guaranteed response time; this is a small, independently maintained project. We will credit you if you want credit, and we will not publish details before a fix is available.

## Scope

In scope:

- the LaunchGrade CLI, MCP server, GitHub Action and site
- parsing bugs that can execute code, read local files, or exfiltrate data
- XSS in generated HTML reports
- supply-chain issues in the release process
- authentication or authorization bugs in project infrastructure

Out of scope:

- findings that require a compromised machine, browser extension, or admin account
- missing security headers on a static site with no accounts or cookies
- automated scanner output without a demonstrated impact
- social engineering
- denial of service by scanning a large public page (use a reasonable URL)

## Safe use of LaunchGrade

LaunchGrade fetches a public URL and a few small well-known files. It does not submit forms, log in, or execute JavaScript from the page.

- Audit pages you own or have permission to test.
- Localhost and private-network URLs are allowed for development, but treat their content as sensitive: a report can contain page copy.
- Generated HTML reports escape page content, but review a report before publishing it if the target page contains untrusted text.
- Never put tokens, passwords or private keys in a URL you audit. They end up in shell history, logs and reports.

## Dependencies

LaunchGrade intentionally has **zero runtime dependencies**. The GitHub Action uses pinned major versions of official Actions. Dependabot watches the workflow files.

Thank you for helping keep the tools safe.
