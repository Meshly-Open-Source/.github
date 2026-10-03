# Meshly Open Source

**[Meshly](https://meshly.ai) is the automation and governance layer that lets
customers connect to their systems of record** — and then holds those
connections to account: provenance for every field, an audit trail for every
change, and reconciliation across sources that disagree.

Connecting is the easy part. Knowing *where a number came from*, *who changed
it*, and *which of two systems to believe* is the part that makes the
connection worth having.

[meshly.ai](https://meshly.ai) · **SOC 2** · [the product](https://validate.meshly.ai)

## The two products

### Meshly Intelligence

**Finds the mismatches, disconnects and problems that exist *between* your
source systems, and helps you reconcile them.**

Two systems that each look internally consistent will still disagree with each
other — a contract value that does not match the invoice, a customer that
exists in the CRM and not the ledger, a renewal date two systems have moved
independently. Nobody owns the gap, because it is not inside either system.
Intelligence is what looks at the gap.

### Meshly Validate

**Applies your policies to open documents — PDFs and the rest — for policy
compliance, and extracts fields for validation and for feeding into other
systems.**

It handles complex treatments rather than only simple field-matching: **ASC 606
revenue-recognition accounting treatment** is the worked example, where the
answer depends on reading the contract rather than on reading one field in it.

→ [validate.meshly.ai](https://validate.meshly.ai)

## Systems we connect to

| | |
|---|---|
| **CRM** | [Salesforce](https://www.salesforce.com), [HubSpot](https://www.hubspot.com), [Microsoft Dynamics](https://www.microsoft.com/dynamics-365) |
| **Accounting / ERP** | [Xero](https://www.xero.com), [QuickBooks](https://quickbooks.intuit.com), [NetSuite](https://www.netsuite.com) |
| **Banking** | [Revolut](https://www.revolut.com) |
| **Documents & e-signature** | [DocuSign](https://www.docusign.com) |
| **Payments** | *coming soon* — [Stripe](https://stripe.com) and others |

Depth varies by connector, and we would rather say so than imply parity. This
list is derived from the connector modules that actually exist, not from a
roadmap.

## Compliance

Meshly is **SOC 2** compliant. Multi-tenant isolation, audit events carrying
tenant identity, and per-tenant rate limiting are treated as properties the
code enforces rather than policies a document asserts — which is also why the
open-source work here leans so hard on *gates* over *conventions*.

For security reports against anything in this organisation, see the
`SECURITY.md` in the relevant repository, or email `security@meshly.ai`. Please
do not open a public issue for a vulnerability.

## What lives in this organisation

This is the **open-source** side of Meshly: the pieces that are generally
useful, published because they are useful to other people and not because they
are a product.

| Repository | What it is |
|---|---|
| [**google-cloud-github-runner**](https://github.com/Meshly-Open-Source/google-cloud-github-runner) | A [soft fork](https://github.com/Meshly-Open-Source/google-cloud-github-runner#how-soft-is-this-fork-honestly) of [Cyclenerd/google-cloud-github-runner](https://github.com/Cyclenerd/google-cloud-github-runner) — ephemeral just-in-time self-hosted [GitHub Actions](https://docs.github.com/actions) runners on Google Cloud. Adds a framework-agnostic IP allowlist and self-hosting notes. |

A deliberately small list. The things here share a shape: infrastructure we
needed, built to be given away rather than to advertise. Expect tooling and
libraries rather than the product — **the product is not open source and this
organisation does not pretend otherwise.**

> **A note on how this code is written.** Much of what we publish here is
> written by AI coding agents under human review, and our repositories
> [say so plainly](https://github.com/Meshly-Open-Source/google-cloud-github-runner#%EF%B8%8F-ai-generated-code-disclosure)
> in their READMEs. A maintainer or adopter deciding whether to trust or review
> code is entitled to know how it was produced; finding out afterwards is worse
> for everyone. Where we contribute upstream to someone else's project, the
> pull request says it too.

## Why open source, when the product is not

> *"By working together, pooling our resources and building on our strengths,
> we can accomplish great things."*
> — **Ronald Reagan** (1984)

> *"To whom much is given, much will be required."*
> — **Luke 12:48**

> *"No one can whistle a symphony. It takes a whole orchestra to play it."*
> — **H. E. Luccock**

> *"If you want to go fast, go alone. If you want to go far, go together."*
> — **African proverb**

Nearly everything we run is built on work someone else gave away — [Python](https://www.python.org),
[Flask](https://flask.palletsprojects.com), [OpenTofu](https://opentofu.org),
and a long tail besides. Publishing the generally-useful parts is how that
account gets settled, and the honest reason it is a small list is that most of
what we build is specific to us and would waste your time.

Where we fork another project, we **track** it rather than diverge from it, and
we send fixes **upstream** rather than keeping them: a fix landed upstream
reaches everyone running that software, and a fix kept in a fork reaches only
us. Everything we publish is [Apache-2.0](https://www.apache.org/licenses/LICENSE-2.0)
unless a repository says otherwise.

---

[meshly.ai](https://meshly.ai) · [validate.meshly.ai](https://validate.meshly.ai) · `security@meshly.ai`
