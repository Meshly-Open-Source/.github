# Meshly Open Source

**[Meshly.ai](https://meshly.ai) is a commercial SaaS service that provides the
automation and governance layer that lets customers connect to their systems of
record and then finds gaps**: provenance (deep linking when possible) for every
field, an audit trail for every ingestion and change, and reconciliation across
sources that disagree.

**For people and agents**, including MCP querying for Claude and OpenAI
models. Agents get the same provenance and tenant boundary as people.

You get **the benefits of a virtual data engineering team**: the integration
work, the pipelines, the reconciliation logic and the audit evidence, without
hiring for any of it.

Meshly understands your vendors' native file formats and APIs, and keeping that
current is part of the service. When a vendor changes an export or an API, that
is our problem; when a vendor adds new capabilities, you get them without doing
the work. Raw pulls are enriched with metadata and with Meshly's
interpretation. Your business policies live in Meshly and are applied on every
ingestion. Ad hoc and custom reporting runs over the result.

**[Meshly.ai](https://meshly.ai) is a SOC 2 certified SaaS provider.** Built
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
<summary>🧩 <strong>Open standards</strong></summary>

Meshly uses open standards, not a proprietary representation:

- **JSON-LD** for linked, self-describing records
- **CloudEvents** for the event envelope
- **schema.org** and the **gist** upper ontology for shared vocabulary
- Open Knowledge Foundation conventions where they fit

Your data stays portable and readable by tools that are not ours, including the
provenance and audit records.

</details>

<details>
<summary>🔌 <strong>Supported integrations</strong></summary>

| | |
|---|---|
| **CRM** | Salesforce, HubSpot, Microsoft Dynamics |
| **Accounting / ERP** | Xero, QuickBooks, NetSuite |
| **Banking** | Revolut |
| **Payments** | Revolut; Stripe and others *coming soon* |
| **Documents & e-signature** | DocuSign |
| **Files** | PDF, CSV |
| **MCP (agents)** | Claude Code, claude.ai, ChatGPT web UI. Single accounts through team and enterprise |
| **Custom** | Internal databases, file drops, in-house APIs |

Depth varies by connector. This list reflects what is built, not a roadmap.

</details>

## Meshly Customer Types & Use Cases

<details>
<summary>🧾 <strong>Audit and accounting firms</strong></summary>

Testing and sampling across client systems,
with the evidence attached to each finding. ASC 606 and similar treatments
applied from your own policies. Per-client separation with one administration
surface.

</details>

<details>
<summary>☁️ <strong>SaaS providers</strong></summary>

Billing, CRM and ledger rarely agree on customer counts or
revenue. Meshly finds where they diverge and shows which source to believe.

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
<summary>👥 <strong>Contractors and BPO</strong></summary>

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

---

# The open-source side

Everything above is the commercial product. Everything below is what we
publish, and the two are not the same thing.

This organisation holds pieces that are generally useful to other people.
It is a short list, and it is infrastructure we needed ourselves.

**The product is not open source.**

| Repository | What it is |
|---|---|
| [**google-cloud-github-runner**](https://github.com/Meshly-Open-Source/google-cloud-github-runner) | Meshly's enhanced fork of [Cyclenerd/google-cloud-github-runner](https://github.com/Cyclenerd/google-cloud-github-runner), used by Meshly's github.com tenant for remote runners on GCP. Ephemeral just-in-time self-hosted runners; adds a framework-agnostic IP allowlist and self-hosting notes. |

<details>
<summary>🤖 <strong>How this code is written</strong></summary>

Much of what we publish here is **written by AI coding agents under human
review**. Our repositories say so, and so do any pull requests we send
upstream.

We state what was verified — tests, linters, mutation runs — separately from
what was not.

</details>

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

[meshly.ai](https://meshly.ai) · `security@meshly.ai`
