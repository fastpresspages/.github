# Contributing to FastPress Labs

Thanks for wanting to make launch tools less boring and more useful.

We keep the surface small on purpose. Before opening a large PR, open an issue or a discussion and describe the user problem. A small, tested patch that fixes one real thing is more likely to land than a rewrite.

## Ground rules

- Be direct, be kind, assume good intent.
- **No fake metrics, fake users, fake testimonials, fake logos or fake partnerships.** This is a hard rule, not a style preference.
- **No dark patterns.** No fake scarcity, hidden opt-ins, pre-checked consent, or copy that hides the price.
- **No telemetry.** Tools should not phone home. If a feature needs a network call, it must be visible and documented.
- **No new dependencies without a strong reason.** LaunchGrade is deliberately zero-dependency. A dependency PR needs to explain why the platform or standard library cannot do the job.
- **Public pages only.** Do not build features that scan private dashboards or bypass authentication.

## Where to start

| You want to… | Go here |
| --- | --- |
| Report a bug | Open a bug issue with the URL, command, expected and actual result |
| Propose a check | Open a "check idea" issue with the failure mode and a concrete fix |
| Fix something small | Look for `good first issue` |
| Improve docs | PRs welcome; keep claims accurate and dated when they are measurements |
| Report a security issue | **Do not open a public issue.** Follow [SECURITY.md](SECURITY.md) |
| Propose a collaboration | Email [meetcode99@gmail.com](mailto:meetcode99@gmail.com) |

## Development

LaunchGrade is plain Node.js (18.17+) with no build step and no runtime dependencies.

```bash
git clone https://github.com/fastpresspages/launchgrade.git
cd launchgrade
node --test
node bin/launchgrade.js https://fastpresspages.github.io/launchgrade/
```

Useful commands:

```bash
node --test                 # full test suite
node bin/launchgrade.js --list
node scripts/serve.js 4173  # preview the site locally
```

On Windows, `npm.ps1` may be blocked by the execution policy. Call `node` directly or use `npm.cmd`.

## Adding or changing a check

Each check is an object in `src/checks.js` with:

- a unique `id`, prefixed by category (`conv.`, `trust.`, `tech.`, `seo.`, `social.`, `a11y.`, `agent.`)
- a `category`, `weight` (1–3), `title`, `detail` and a concrete `fix`
- a `run(ctx)` function returning `pass`, `warn`, `fail`, `info` or `skipped`
- no network calls of its own; use the context the fetcher already built
- no side effects and no writes outside the report directory

If you add a scored check, add a fixture and a test that proves both the passing and failing case. If the check is informational, return `info` and explain why it does not affect the score.

Checks should reward real user value, not keyword presence. "Has a privacy policy" is useful. "Mentions the word privacy three times" is not.

## Tests and reports

- Run `node --test` before opening a PR.
- Keep reports deterministic enough to review; dates and response times are expected to vary.
- If you change scoring, update `README.md`, `site/llms-full.txt` and any sample reports that would become wrong.
- Do not commit a generated report as proof of a grade you did not actually get. Date it honestly.

## Pull requests

A good PR includes:

1. The user problem, in one paragraph.
2. What changed and what did not.
3. The commands you ran and the result.
4. Screenshots for visual changes.
5. Any trade-offs or follow-up work.

Small PRs can be squashed. Large PRs should explain the shape before the diff.

## Commit style

Short imperative subject, then context if needed:

```text
Add llms.txt discovery fallback for project pages
Fix form label count when a honeypot is present
```

## License

By contributing, you agree that your contribution is licensed under the Apache License 2.0, the same license as the project.
