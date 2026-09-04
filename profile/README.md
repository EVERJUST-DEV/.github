<h1 align="center">EVERJUST-DEV</h1>

<p align="center">
  <strong>EVERJUST-DEV is the organization where EVERJUST's production software lives —
  the mail infrastructure every product sends through, and the products that send on it.</strong>
</p>

<p align="center">
  <a href="https://everjust.app">EVERJUST.APP</a> ·
  <a href="https://customagents.io">Custom Agents</a> ·
  <a href="https://customdomain.ai">Custom Domain</a> ·
  <a href="https://customportal.app">CustomPortal</a> ·
  <a href="https://justpost.app">JustPost</a>
</p>

<p align="center">
  <a href="https://mail.everjust.app/docs/"><img alt="Docs" src="https://img.shields.io/badge/docs-mail.everjust.app-1D1D1F?style=flat"></a>
  <a href="https://status.customagents.io"><img alt="Status" src="https://img.shields.io/badge/status-status.customagents.io-1D1D1F?style=flat"></a>
  <a href="https://github.com/ever-just"><img alt="Portfolio" src="https://img.shields.io/badge/portfolio-github.com/ever--just-1D1D1F?style=flat"></a>
</p>

---

> [!NOTE]
> The `-DEV` in the name is a GitHub name collision, not a stage gate. `EVERJUST` was already
> taken by an unrelated account, so the suffix is permanent. Everything in here is production.

## About this organization

EVERJUST builds and operates the software a small company runs on: the workspace the business
lives in, agents that answer its customers, and the domain, mail and portal layers underneath.

Most of this organization is private, because most of it is running software with customers on
it. What is open is the part that stands on its own for somebody who has never heard of us —
starting with the email infrastructure, which is the piece we most wanted to find already built
when we went looking for it and did not.

## Open

| Repository | What it is |
|---|---|
| [usesend-email](https://github.com/EVERJUST-DEV/usesend-email) | Self-hosted, multi-tenant transactional email on Amazon SES: Terraform for the AWS stack, an MCP server so agents can send, and the docs to run the whole thing yourself. It is what sends EVERJUST's own mail, live at [mail.everjust.app](https://mail.everjust.app). SES bills per email and never per domain, which is the entire reason it exists. |
| [.github](https://github.com/EVERJUST-DEV/.github) | This profile, plus the organization's shared community-health files. |

## Private

| Repository | What it is | Live |
|---|---|---|
| **JustMail** | Self-hosted email, contacts and chat on Odoo 19 — three add-ons plus an inbound SES gateway, server-side rules and filters, a unified inbox, and an SPF/DKIM/DMARC setup screen that parses records rather than string-matching them. | — |
| **JustPost** | Social publishing and scheduling. An AGPL-3.0 fork of Postiz with EVERJUST's LinkedIn Pages wiring, AI provider configuration and deploy path. | [justpost.app](https://justpost.app) |

## The rest of the estate

These are EVERJUST products whose code sits outside this organization. Closed repositories are
listed by product and live URL rather than by a link that would 404 for you.

- **[EVERJUST.APP](https://everjust.app)** — a multi-tenant business workspace: one shared customer
  record across the apps, and a PostgreSQL database per organization at `<org>.everjust.app`.
  Self-serve signup since July 2026. Closed source.
- **[Custom Agents](https://customagents.io)** — agents with their own email address, phone number
  and Slack profile, holding one thread per customer across email, SMS and iMessage, Slack,
  Instagram and voice. [Live status](https://status.customagents.io). Closed source.
- **[Custom Domain](https://customdomain.ai)** — let your users bring a domain they already own and
  get it live with HTTPS. The SDK, the MCP server and the [docs](https://docs.customdomain.ai/docs)
  are public in their own organization: [CUSTOM-DOMAIN-APP](https://github.com/CUSTOM-DOMAIN-APP).
- **[CustomPortal](https://customportal.app)** — a white-label client portal a firm runs under its
  own name, with a database per tenant. Closed source.
- **[agentskills](https://github.com/ever-just/agentskills)** — the agent skill library the work
  above is actually built with. Public, MIT, and clonable on its own.

## How this organization is run

- **Every repository carries a description and topics.** A repository nobody can identify from the
  list page is not finished.
- **Repositories are archived, not deleted**, when there are no active maintainers, when issues or
  pull requests have gone unanswered for six months, when there have been no commits in a year, or
  when the work has been folded into another repository.
- **Secrets stay out of git.** Deploys authenticate with GitHub OIDC and IAM roles rather than
  long-lived keys, and anything that must be a secret lives in a secret manager.
- **Public repositories carry runnable instructions**, not a description of instructions. If the
  quickstart in a README does not work on a clean machine, that is a bug in the README.

Portfolio, tooling and public research: **[github.com/ever-just](https://github.com/ever-just)** ·
Contact: **company@everjust.co**
