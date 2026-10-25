# How I build

I write most of my code with Claude Code, and nearly every commit in my private repos is co-authored with it. I'm open
about that.

What the AI doesn't decide is what to build, what "correct" means, or whether something is safe to turn on. That part
is mine, and it's most of the work.

## What I own

- **The problem and the rules.** I run the technology and finance side of a plumbing company. I know how a commission is
  earned, why a deposit doesn't match a payout, and what a technician needs on a phone at a customer's door. Those rules
  become specs, settings and tests.
- **The architecture.** One sign-in for every tool, one access-control service, one database per tool, and shared
  internal services for ServiceTitan data, AI and phones. I decide those boundaries and hold them.
- **Acceptance.** I decide what done means (a passing test, a real phone call, a reconciliation that ties to the cent)
  and check it on the real system before it ships.
- **Production.** Deploys, rollbacks, secrets, backups, and the switches that turn risky features on.

## The workflow

1. **Write it down first.** Each tool starts as a written plan in its repo: the problem, the users, the data, the rules
   and what's out of scope.
2. **Make every repo readable by an agent.** Each repo has an `AGENTS.md`/`CLAUDE.md` with its conventions and hard
   rules, and a `docs/HANDOFF.md` with current state and open work, so any session can pick up any tool cold.
3. **Tests are the contract.** Business rules are unit-tested, outside APIs are tested against recorded real responses,
   the phone system is tested with real calls placed through headless browsers, and the AI receptionist has to pass a
   set of example conversations before it can deploy.
4. **Safety gates are code.** Writes to outside systems start in dry-run. Customer-facing sending stays off until an
   owner turns it on. Production deploys refuse to run from a checkout that's behind GitHub or if they would blank a
   server secret.
5. **Business choices are settings.** Thresholds, schedules, scripts and ring orders are settings on a screen with
   version history, so changing how the business runs doesn't need a deploy.
6. **Verify on the real thing.** Phone timing is measured on real calls, backups are proven by restoring them, and the
   books are proven by reconciling to bank statements rather than trusting a report.

## Larger jobs

For bigger pieces of work I split the job across several agent sessions that share one written contract, then run a
separate review pass whose only job is to find what the others got wrong.

## Fundamentals

I keep practicing by hand so I can read, judge and debug what agents write: the Boot.dev back-end path (in progress),
small Go and Python projects written without AI, and pull requests to other people's projects, where the maintainers
are the reviewers. See [OPEN-SOURCE.md](OPEN-SOURCE.md).
