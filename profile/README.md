# Meshly Open Source

**[Meshly.ai](https://meshly.ai) is a commercial SaaS service that provides the
automation and governance layer that lets customers connect to their systems of
record** — and then holds those connections to account: provenance for every
field, an audit trail for every change, and reconciliation across sources that
disagree.

**For people *and* agents**, including
[MCP](https://modelcontextprotocol.io) querying capabilities for
[Claude](https://claude.ai) and [OpenAI](https://openai.com) models — so an
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

<details>
<summary>📊 <strong>Meshly Intelligence</strong> — find and reconcile what your systems disagree about</summary>

**Finds the mismatches, disconnects and problems that exist *between* your
source systems, and helps you reconcile them.**

Two systems that each look internally consistent will still disagree with each
other: a contract value that does not match the invoice, a customer that exists
in the CRM and not the ledger, a renewal date two systems have moved
independently.

Nobody owns the gap, because the gap is not inside either system. The team that
owns the CRM sees clean CRM data. The team that owns the ledger sees a clean
ledger. Intelligence is what looks at the space between them, tells you which
source to believe, and shows the working.

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

→ **[validate.meshly.ai](https://validate.meshly.ai)**

</details>

<details>
<summary>🔌 <strong>Systems we connect to</strong></summary>

| | |
|---|---|
| **CRM** | [Salesforce](https://www.salesforce.com), [HubSpot](https://www.hubspot.com), [Microsoft Dynamics](https://www.microsoft.com/dynamics-365) |
| **Accounting / ERP** | [Xero](https://www.xero.com), [QuickBooks](https://quickbooks.intuit.com), [NetSuite](https://www.netsuite.com) |
| **Banking** | [Revolut](https://www.revolut.com) |
| **Payments** | [Revolut](https://www.revolut.com); [Stripe](https://stripe.com) and others *coming soon* |
| **Documents & e-signature** | [DocuSign](https://www.docusign.com) |

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
| [**google-cloud-github-runner**](https://github.com/Meshly-Open-Source/google-cloud-github-runner) | A soft fork of [Cyclenerd/google-cloud-github-runner](https://github.com/Cyclenerd/google-cloud-github-runner) — ephemeral just-in-time self-hosted [GitHub Actions](https://docs.github.com/actions) runners on Google Cloud. Adds a framework-agnostic IP allowlist and self-hosting notes. |

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

Nearly everything we run is built on work someone else gave away —
[Python](https://www.python.org), [Flask](https://flask.palletsprojects.com),
[OpenTofu](https://opentofu.org), and a long tail besides. Publishing the
generally-useful parts is how that account gets settled. The honest reason it
is a small list is that most of what we build is specific to us and would waste
your time.

Where we fork another project we **track** it rather than diverge from it, and
we send fixes **upstream** rather than keeping them: a fix landed upstream
reaches everyone running that software, and a fix kept in a fork reaches only
us.

Everything we publish is
[Apache-2.0](https://www.apache.org/licenses/LICENSE-2.0) unless a repository
says otherwise.

</details>

---

[meshly.ai](https://meshly.ai) · [validate.meshly.ai](https://validate.meshly.ai) · `security@meshly.ai`
