# Meshly Open Source

**Meshly is the automation and governance layer that lets customers connect to
their systems of record** — and then holds those connections to account:
provenance for every field, an audit trail for every change, and reconciliation
across sources that disagree.

Connecting is the easy part. Knowing *where a number came from*, *who changed
it*, and *which of two systems to believe* is the part that makes the
connection worth having.

## Systems we connect to

| | |
|---|---|
| **CRM** | Salesforce, HubSpot, Microsoft Dynamics |
| **Accounting / ERP** | Xero, QuickBooks, NetSuite |
| **Banking** | Revolut |
| **Documents & e-signature** | DocuSign |
| **Payments** | *coming soon* — Stripe and others |

Depth varies by connector, and we would rather say so than imply parity. This
list is derived from the connector modules that actually exist, not from a
roadmap.

## What lives in this organisation

This is the **open-source** side of Meshly: the pieces that are generally
useful, published because they are useful to other people and not because they
are a product.

It is deliberately a small list, and the things here share a shape — they are
infrastructure we needed, built to be given away rather than to advertise.

Expect to find tooling and libraries rather than the product. The product is
not open source and this organisation does not pretend otherwise.

> **A note on how this code is written.** Much of what we publish here is
> written by AI coding agents under human review, and our repositories say so
> plainly in their READMEs. A maintainer or adopter deciding whether to trust
> or review code is entitled to know how it was produced; finding out
> afterwards is worse for everyone. Where we contribute upstream to someone
> else's project, the pull request says it too.

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

Nearly everything we run is built on work someone else gave away. Publishing
the generally-useful parts is how that account gets settled — and the honest
reason it is a small list is that most of what we build is specific to us and
would waste your time.

Where we fork another project, we track it rather than diverge from it, and we
send fixes **upstream** rather than keeping them: a fix landed upstream reaches
everyone running that software, and a fix kept in a fork reaches only us.

---

[meshly.ai](https://meshly.ai)
