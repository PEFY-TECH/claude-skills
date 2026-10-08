# PEFY-GG UI UX Pro Max — Activation & Assurance Register

**As-of:** 2026-10-08 (UTC). **Sponsor:** Dr Erick Franck PATHINVO / PEFY-GG. **Operational owner:** PEFY-TECH.
**Scope of this record:** GitHub-repository governance/CI integration only; no claim of account-wide ChatGPT or developer-device installation.

## 1. Deployed artifacts

| Surface | Committed state | Qualification |
| --- | --- | --- |
| Personal GitHub fork | `yemanlin1st/ui-ux-pro-max-skill`, PR #1 merged, squash SHA `c6e5625c8524e7c30237f27cf6ee320706b347de` | Verified repo-local `.agents/skills/ui-ux-pro-max/SKILL.md`; initial static check passed in Actions |
| PEFY-TECH governance repository | `PEFY-TECH/claude-skills`, PR #1 merged, squash SHA `7bccca60e61ff9824444221276cb88cc5e277ed2` | Canonical governance skill and Codex discovery shim committed to `main` |
| PEFY-TECH upstream engine CI smoke | Pinned `ui-ux-pro-max-cli@2.15.0` in ephemeral GitHub Actions | Official CLI installation, script presence, actual design-system query, package metadata and high-severity npm audit all passed on run **37824768703** |

**Source of official package:** https://github.com/nextlevelbuilder/ui-ux-pro-max-skill , MIT.
**Official release checked:** v2.15.0 (GitHub published 2026-08-13).
**Approved npm package:** `ui-ux-pro-max-cli@2.15.0`.
**Approved published npm SHA512 integrity metadata:**
`sha512-D0J/C40xrzzi5si6ZLtRGbEE5v3QjL7d4wJNnasmP3yfDSrGiuqVCdwQiqCNnIkbqOuVoA/uonR2o1WKXh3urw==`.
The CI workflow pins/checks this exact value and runs a weekly dependency/design-system smoke; installation is scoped to a disposable runner. A matching registry metadata value is *not* a proof of publisher identity or an independent security audit.

## 2. Evidence matrix and limitations

| Control | Evidence | Result |
| --- | --- | --- |
| Third-party license inspected | Upstream `LICENSE` (MIT) | Verified at source |
| Upstream origin and tag established | Official GitHub releases and latest tag v2.15.0 | Verified at assessment date |
| npm package name/version | GitHub Actions CI metadata check | Pass |
| npm SHA512 metadata lock | GitHub Actions exact-match check | Conditional on current run; earlier CI checked prefix only |
| High-severity *known* runtime dependency advisories | `npm audit --omit=dev --audit-level=high` in CI | Pass at run 37824768703; repeat weekly |
| Official CLI installation and design-system search | `npx ... init --ai universal --offline` plus `search.py ... --design-system` | Pass in CI run 37824768703 |
| PEFY-TECH repo skill recognized as source artifact | Fetched `.agents/skills/pefy-uiux-governed-design/SKILL.md` on main | Verified |
| Personal Codex host installed/running | No Codex environment registered at assessment | **NOT VERIFIED** |
| User machine installed/running | No Desktop Commander device connected at assessment | **NOT VERIFIED** |
| ChatGPT personal account skill installation | Skills entitlement may not cover Plus plan | **NOT AVAILABLE / NOT VERIFIED** |
| Product-specific rollouts and UX audits | No individual app project designated or qualified | **NOT VERIFIED** |
| Real production user traffic or full security qualification | No production host/access/test evidence | **NOT VERIFIED** |

CI passing is *not* WCAG 2.2 AA conformance, nor app-level acceptance, nor a regulated-domain license.

## 3. Activation model

1. **Source promotion:** merged PRs and ability to discover `SKILL.md` in the relevant GitHub checkout.
2. **GitHub CI:** npm integrity checked, official CLI installed in temporary workspace, core UI/UX reasoning invoked, known dependencies audited for high or critical advisories.
3. **Developer environment:** admin/operator connects an authorized machine or Codex environment, installs approved release, verifies skill loading. Must be done separately because no environment is registered.
4. **Product repositories:** each approved product gets a scoped integration PR, local task-flow tests, WCAG and security checks, product-specific design tokens, and acceptance evidence.
5. **ChatGPT workspace:** only if the workspace's eligibility and administrator controls allow custom Skills; user/admin installs through supported UI. Do not infer from GitHub merge.

## 4. Operations, incident & rollback

- Version policy: approved exact release with explicit SHA512; no automatic unreviewed dependency upgrades.
- Scheduled CI: weekly smoke/audit; fails when current package or dependencies become unqualified. New releases are evaluated separately and promoted by reviewed PR.
- If the workflow fails, treat this integration as `DEGRADED` for CI use; inspect failed step, advisories or registry integrity drift before re-enabling.
- Rollback source: revert the PEFY-TECH squash commit `7bccca60e61ff9824444221276cb88cc5e277ed2` or the subsequent security hardening commit through approved PR, retaining evidence.
- Rollback local: `uipro uninstall --ai codex` under the relevant project only after identifying scope and backing up conflicts.
- No automatic access to sensitive customer data, production credentials, financial transactions or security control changes.
- Follow ΩCSF R2.0, ΩAEIF lifecycle gates, ΩRCIAF dynamic applicability, ΩVIF/ΩWEBFORGE governance.

## 5. Operational acceptance gates

- [x] GitHub provenance and author attribution identified
- [x] Repo-local manifests and canonical policy committed
- [x] Official CLI exercised in ephemeral CI runner
- [x] CI audit and design-system smoke green on PR
- [x] Two GitHub staging PRs merged
- [ ] Main-branch CI with SHA512 lock passes
- [ ] Native Codex developer environment connected and skill invocation verified
- [ ] ChatGPT Skill creation/installation completed if account/workspace eligible
- [ ] Each in-scope product repo activated with separate evidence
- [ ] End-user performance/accessibility/security validated in production environment

**Assessment:** **GitHub source and CI integration ACTIVE; portfolio / ChatGPT / developer host PRODUCTION ACTIVATION NOT YET VERIFIED.**
