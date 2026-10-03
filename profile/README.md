# Meshly Open Source

**[Meshly.ai](https://meshly.ai) is a commercial SaaS service that provides the
automation and governance layer that lets customers connect to their systems of
record** — and then holds those connections to account: provenance for every
field, an audit trail for every change, and reconciliation across sources that
disagree.

**For people *and* agents**, including
MCP querying capabilities for
Claude and OpenAI models — so an
agent asking about your data gets the same provenance and the same tenant
boundary a person does, rather than a convenient answer with no lineage.

In practice you get **the benefits of a virtual data engineering team**: the
integration work, the pipelines, the reconciliation logic and the audit
evidence, without hiring for any of it. The work that normally lands on whoever
is least busy, done as a service.

**[Meshly.ai](https://meshly.ai) is a SOC 2 certified SaaS provider.** Built
for the midmarket, light enough for small teams, and architected to scale to
very large use cases — multi-tenant isolation, per-tenant rate limiting and
tenant-scoped audit events are properties the code enforces rather than
policies a document asserts.

## Meshly Capabilities

<details>
<summary>📊 <strong>Meshly Intelligence</strong> — find and reconcile what your systems disagree about</summary>

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
<summary>📄 <strong>Meshly Validate</strong> — your policies, applied to open documents</summary>

**Applies your policies to open documents — PDFs and the rest — for policy
compliance, and extracts fields for validation and for feeding into other
systems.**

It handles complex treatments rather than only simple field-matching.
**ASC 606 revenue-recognition** is the worked example: the answer depends on
reading the contract, not on reading one field in it — performance
obligations, variable consideration and allocation are judgements about the
whole document.

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
| **Custom** | Bespoke sources — internal databases, flat-file drops, in-house APIs, anything with a contract we can read |

Depth varies by connector and we would rather say so than imply parity. This
list is derived from the connector modules that exist, not from a roadmap.

</details>

---

# The open-source side

Everything above is the commercial product. Everything below is what we
publish, and the two are not the same thing.

This organisation holds the pieces that are **generally useful** — published
because they are useful to other people, not because they are a product. A
deliberately small list, sharing one shape: infrastructure we needed, built to
be given away rather than to advertise.

**The product is not open source and this organisation does not pretend
otherwise.**

| Repository | What it is |
|---|---|
| [**google-cloud-github-runner**](https://github.com/Meshly-Open-Source/google-cloud-github-runner) | Meshly's enhanced fork of [Cyclenerd/google-cloud-github-runner](https://github.com/Cyclenerd/google-cloud-github-runner), used by Meshly's github.com tenant for remote runners on GCP. Ephemeral just-in-time self-hosted runners; adds a framework-agnostic IP allowlist and self-hosting notes. |

<details>
<summary>🤖 <strong>How this code is written</strong> — AI authorship, stated plainly</summary>

Much of what we publish here is **written by AI coding agents under human
review**, and our repositories say so in their READMEs rather than leaving you
to infer it from the commit style.

A maintainer or adopter deciding whether to trust or review code is entitled to
know how it was produced; finding out afterwards is worse for everyone. Where
we contribute upstream to someone else's project, the pull request says it too.

We also try to state what was **verified** separately from what was merely
written — a passing test suite, a clean linter, mutations that turn the suite
red — and to keep an honest list of what was *not* checked.

</details>

<details>
<summary>🔐 <strong>Reporting a security issue</strong></summary>

**Please do not open a public issue for a vulnerability.**

Use the `SECURITY.md` in the relevant repository, or email
**`security@meshly.ai`**. Each repository's policy says which paths are ours
and which belong to an upstream project, because a report filed in the wrong
place looks tracked while nobody who can fix it is reading it.

Two bug classes we especially want, where our code is fail-closed: a **bypass**,
and a **silent total denial** — anything that makes a control deny everything
without that being evident. The second is reported far less and matters just as
much, because "nothing is being accepted" looks identical to "nobody is
calling us".

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
