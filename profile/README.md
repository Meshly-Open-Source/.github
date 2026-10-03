# [Meshly.AI](https://www.meshly.ai)

**[Meshly.AI](https://www.meshly.ai) is a commercial SaaS service that provides the
automation and governance layer that lets customers connect to their systems of
record — CRMs like HubSpot and Salesforce, accounting systems like Xero,
QuickBooks and NetSuite, and whatever else you run — and then finds gaps**:
provenance (deep linking when possible) for every field, an audit trail for
every ingestion and change, and reconciliation across sources that disagree.

**For people and agents**, including MCP querying for Claude and OpenAI
models. Agents get the same provenance and tenant boundary as people.

You get **the benefits of a virtual data engineering team**: the integration
work, the pipelines, the reconciliation logic and the audit evidence, without
hiring for any of it.

[![Meshly in Times Square](https://img.youtube.com/vi/Jcas-r2eITQ/maxresdefault.jpg)](https://www.youtube.com/watch?v=Jcas-r2eITQ)

*Meshly in Times Square*

## How Meshly works

**[See how it works →](https://www.meshly.ai/#how-it-works)**

Meshly understands your vendors' native file formats and APIs, and keeping that
current is part of the service. When a vendor changes an export or an API, that
is our problem; when a vendor adds new capabilities, you get them without doing
the work. Raw pulls are enriched with metadata and with Meshly's
interpretation. Your business policies live in Meshly and are applied on every
ingestion. Ad hoc and custom reporting runs over the result.

**[Meshly.AI](https://www.meshly.ai) is a SOC 2 certified SaaS provider.** Built
for the midmarket, light enough for small teams, and architected to scale to
very large use cases. Multi-tenant isolation, per-tenant rate limiting and
tenant-scoped audit events are enforced in code.

## Meshly Capabilities

<details>
<summary>📊 <strong>Meshly Intelligence</strong></summary>

**Finds the mismatches, disconnects and problems that exist *between* your
source systems, and helps you reconcile them.**

Ever have data that disagreed between two systems? Have 998 customers in your
accounting system but 1,000 in Salesforce as closed/won?

Gaps persist despite vendor improvements, because they are different systems
from different vendors. Meshly can help reduce the load by healing incomplete
or cleaning dirty data, using a combination of classical data science, machine
learning, and frontier models from leading vendors like Anthropic, OpenAI and
Google.

</details>

<details>
<summary>📄 <strong>Meshly Validate</strong></summary>

**Applies your policies to open documents — PDFs and the rest — for policy
compliance, and extracts fields for validation and for feeding into other
systems.**

It handles complex treatments, not just field matching. **ASC 606
revenue-recognition** is one example: performance obligations, variable
consideration and allocation all depend on the whole contract.

</details>

<details>
<summary>🔌 <strong>Supported integrations</strong></summary>

| | |
|---|---|
| **CRM** | Salesforce, HubSpot, Microsoft Dynamics 365 |
| **Accounting / ERP** | Xero, QuickBooks, NetSuite |
| **Banking** | Revolut |
| **Payments** | Revolut; Stripe and others *on request* |
| **Documents & e-signature** | DocuSign |
| **Files** | PDF, CSV, and whatever shape your vendor invented |
| **Warehouses** | Google BigQuery; Snowflake secure data sharing and Databricks Delta Sharing *on request* |
| **MCP (agents)** | Claude Code, claude.ai, ChatGPT web UI. Single accounts through team and enterprise |
| **Custom** | Internal databases, file drops, in-house APIs. We work with customers whose core systems are custom-built |

**You do not need a warehouse, or any of these systems.** If your data lives in
spreadsheets and PDF exports, that is a supported setup, not a lesser one.

**If your system is not listed, we build the connector.** Meshly already
supports REST APIs and webhooks, and is compatible with major streaming
protocols as well as batch jobs. Our team can help you through configuration
and permissions.

The systems listed above are **self-service** — a few clicks, by someone on
your team with the right permissions. Items marked *on request* are not built
yet; ask, and they get scheduled against a real customer rather than a
roadmap.

Depth varies by connector. Everything not marked *on request* is built and in
use today.

</details>

<details>
<summary>🧩 <strong>Open standards, and agent access</strong></summary>

**You do not need any of this to use Meshly.** There is a web UI, and most
customers work entirely in it, or with Claude.ai or ChatGPT.com. Connect a
source, read the results, generate reports, fix problem data.

This section is for power users, firms with a development team, and anyone
putting agents to work.

Meshly uses open standards, not a proprietary representation:

- **JSON-LD** for linked, self-describing records
- **[CloudEvents](https://cloudevents.io/)** for the event envelope <sup>[[1]](https://docs.cloud.google.com/eventarc/docs/cloudevents)</sup> <sup>[[2]](https://www.google.com/search?q=consumers+of+cloudevents+salesforce)</sup>
- **[schema.org](https://schema.org/)** and the **[gist](https://www.semanticarts.com/gist/)** upper ontology for shared vocabulary, based on vendor-neutral open standards
- **[Open Knowledge Format](https://github.com/GoogleCloudPlatform/open-knowledge-format)** where it fits

**This is what makes Meshly easy for your AI to consume** — whatever you are
running. Self-describing records mean an agent does not have to be taught your
schema, and linked provenance means it can follow a value back to its source
instead of guessing. Access is through MCP, so the agent gets the same tenant
boundary and the same audit trail as a person.

Built to support emerging standards such as
**[AIUC-1](https://www.aiuc-1.com/)** and
**[ISO 42001](https://www.iso.org/insights/iso-42001-explained)**.

Your data stays portable and readable by tools that are not ours, including the
provenance and audit records.

<sub>[1] [CloudEvents on Google Cloud Eventarc](https://docs.cloud.google.com/eventarc/docs/cloudevents) ·
[2] [Who else consumes CloudEvents](https://www.google.com/search?q=consumers+of+cloudevents+salesforce)</sub>

</details>

## Meshly Customer Types & Use Cases

<details>
<summary>☁️ <strong>SaaS application and platform providers</strong></summary>

Billing, CRM and ledger rarely agree on customer counts or
revenue. Meshly finds where they diverge and shows which source to believe.

</details>

<details>
<summary>🧍 <strong>Solopreneurs</strong></summary>

You have got a bunch of systems, and you have to log in and check them every
day. Meshly can automate routine accounting tasks and create an early warning
system — the equivalent of smoke detectors for your digital systems.

</details>

<details>
<summary>🚀 <strong>Startups and accelerator participants</strong></summary>

No data team required. Connect what
you have, get numbers you can put in front of an investor or an auditor, and
keep the trail that shows where they came from.

</details>

<details>
<summary>🏭 <strong>Traditional businesses</strong></summary>

Older systems, file-based exports, and month-end
close done in spreadsheets. Meshly reads the files you already produce.

</details>

<details>
<summary>🏭 <strong>Manufacturing</strong></summary>

Parts, orders and shipments tracked across an ERP, a WMS and whatever the
supplier sends. Meshly reconciles across them and flags what does not line up.

**We love unique file formats.** Fixed-width extracts, EDI variants, a report
someone built in 1998 that nobody dares change — these are normal inputs.
Teaching Meshly to read one is our work, not yours.

</details>

<details>
<summary>👥 <strong>Firms using contractors and BPO</strong></summary>

Most of the work is finding the mismatches, not fixing
them. Meshly does the finding and hands over a list with the evidence attached,
so the hours go to judgement calls instead of spreadsheet comparison. Every
change keeps an audit trail.

</details>

<details>
<summary>🤖 <strong>RPA users</strong></summary>

Screen-scraping bots break when a vendor ships a UI change, and
the failure is usually silent. Meshly works against APIs and file drops, and
reports when a source stops matching what it used to send.

</details>

<details>
<summary>🏢 <strong>Outsourcing firms and RPA providers</strong></summary>

Enterprise RBAC and multi-org support
keep your sub-customers separate, with the boundaries enforced in code, under
one administration surface. Taking on a new client is a connector and a policy,
not a new team.

</details>

<details>
<summary>🚚 <strong>Supply chain and 3PL</strong></summary>

You already have a provider, but your vendor likely has gaps you are filling in
with manual clicking. Meshly can help fill those gaps, especially in
conjunction with OpenAI, Claude and Google Gemini.

</details>

<details>
<summary>🧾 <strong>Audit and accounting firms</strong></summary>

Testing and sampling across client systems,
with the evidence attached to each finding. ASC 606 and similar treatments
applied from your own policies. Per-client separation with one administration
surface.

</details>

<details>
<summary>🔗 <strong>AI agent integration</strong></summary>

Giving an agent access to your systems of record, with the guardrails that
makes reasonable. Agents connect over MCP and get the same tenant boundary,
the same permissions and the same audit trail as a person.

Every answer carries its provenance, so an agent can show where a number came
from rather than asserting it.

</details>

<details>
<summary>🌍 <strong>Everyone</strong></summary>

Meshly makes AI safer to consume for your business-critical systems:
inspectable, and audit-ready.

</details>
---

# Meshly Labs Open Source

| Repository | What it is | Intended audience |
|---|---|---|
| [**google-cloud-github-runner**](https://github.com/Meshly-Open-Source/google-cloud-github-runner) | Meshly's enhanced fork of [Cyclenerd/google-cloud-github-runner](https://github.com/Cyclenerd/google-cloud-github-runner), used by Meshly's github.com tenant for remote runners on GCP. Ephemeral just-in-time self-hosted runners; adds a framework-agnostic IP allowlist and self-hosting notes. | Users of github.com with CI workflows who want to save money on GitHub runners, as a drop-in replacement |

<details>
<summary>🔐 <strong>Reporting a security issue</strong></summary>

**Please do not open a public issue for a vulnerability.**

Use the `SECURITY.md` in the relevant repository, or email
**`security@meshly.ai`**. Each policy says which paths are ours and which
belong to an upstream project.

For fail-closed code we want two things reported: a **bypass**, and a **silent
total denial** where a control starts refusing everything without that being
visible.

</details>

<details>
<summary>💬 <strong>Why open source, when the product is not</strong></summary>

> *"By working together, pooling our resources and building on our strengths,
> we can accomplish great things."*
> — **Ronald Reagan** (1984)

> *"To whom much is given, much will be required."*
> — **Luke 12:48**

> *"No one can whistle a symphony. It takes a whole orchestra to play it."*
> — **H. E. Luccock**

> *"If you want to go fast, go alone. If you want to go far, go together."*
> — **African proverb**


</details>

---

[meshly.ai](https://www.meshly.ai) · `security@meshly.ai`
