# Shayn Hornik

I co-founded Honey Go Fix It, a residential plumbing company in Dayton, Ohio, in 2022. I'm a licensed Ohio plumbing,
HVAC and refrigeration contractor, and I write the software the company runs on.

Most of that code is private because it handles real customer data, so this repo describes how each piece works instead:
the problem, the design, what went wrong and what I'd change.

[LinkedIn](https://www.linkedin.com/in/shaynhornik) · [GitHub](https://github.com/shaynhornik) · Dayton, Ohio

---

## In daily use

| System | What it does | Case study |
|---|---|---|
| **Phone system and Android app** | The company's phones on Telnyx: call routing, a browser softphone, recordings and transcripts, office texting, and a native Kotlin calling app for staff. | [06](case-studies/06-phone-system.md) |
| **AI receptionist** | Answers the calls the office can't get to and calls after hours, books visits into ServiceTitan and transfers to a person when it should. Rules like "never quote a price" are checked in code on every reply, not left to the prompt. | [07](case-studies/07-emily-ai-assistant.md) |
| **ServiceTitan connection** | A read-only copy of our ServiceTitan data in Postgres that the other tools read from, and one guarded path for writes that starts in dry-run and is switched on one kind at a time. | [02](case-studies/02-servicetitan-replica.md) |
| **Ridealong** | An Android app our technicians use to record in-home visits. Each visit is transcribed and scored against the company's own service steps, with quotes from the visit as evidence. | [09](case-studies/09-ridealong.md) |
| **Books rebuild** | A Python toolkit I used to rebuild the company's books from 2022 and reconcile each account to its bank and card statements. | [04](case-studies/04-books-rebuild.md) |

## Earlier and smaller

- **Performance Center** ([12](case-studies/12-performance-center.md)): KPIs, commissions and weekly payroll for the field team. Used from February to September 2026, then retired when we moved to ServiceTitan.
- **Shared platform** ([01](case-studies/01-hgfi-tools-platform.md)), **AI gateway** ([08](case-studies/08-ai-gateway.md)), **finance and job costing** ([03](case-studies/03-finance-job-costing.md)), **marketing tools** ([10](case-studies/10-marketing-platform.md)), **policies and training** ([11](case-studies/11-playbook.md)), **booking from office calls** ([18](case-studies/18-hands-free-booking.md)) and a **read-only data kit for our office manager** ([05](case-studies/05-analyst-kit.md)).

## Side project

**[FYProof](https://fyproof.com)** ([17](case-studies/17-fyproof.md)), with a partner: a web app that checks a video against
platforms' content rules before it's posted. In public beta.

## Open source

I've had 19 pull requests merged into other people's projects, most of them to
[securo](https://github.com/securo-finance/securo), a self-hosted finance app, plus one each to Apache iceberg-python,
Apache Maka and TheNinjaRPG. The list is in [OPEN-SOURCE.md](OPEN-SOURCE.md).

## How I work

I write most of my code with Claude Code. I write the spec and the business rules, decide what "done" means, test on
the real system and handle the deploys. More in [HOW-I-BUILD.md](HOW-I-BUILD.md). The stack is in [STACK.md](STACK.md).

---

<sub>Closed-source projects are described, not published. No customer, employee or company financial data appears in this repo.</sub>
