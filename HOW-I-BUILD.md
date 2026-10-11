# How I build

I build with AI. Most of the code in my private repos was written by Claude Code working from my specs, and nearly every
commit carries a `Co-Authored-By: Claude` line. I'm not hiding that; it's the reason one person running a company's
finance and IT could ship a dozen production-grade tools in a few weeks.

What AI does not do is decide what to build, what "correct" means, or whether it's safe to turn on. That part is mine,
and it's most of the work.

## What I own

- **The problem and the rules.** I run the finance and IT side of a plumbing company. I know how a commission is
  earned, why a deposit doesn't match a payout, what a technician needs on a phone at a customer's door, and which
  mistakes cost real money. Those rules become specs, settings and tests.
- **The architecture.** One sign-in for every tool, one access-control service, one database per tool, internal services
  for shared data (ServiceTitan, AI, phones), and a set of conventions every repo follows. I decide those boundaries and
  hold them.
- **Acceptance.** I define what done means (a test, a real phone call, a reconciliation that ties to the cent) and I
  verify it on the real system before it ships.
- **Production.** Deploys, rollbacks, secrets, backups, incident fixes, and the switches that turn risky features on.

## The workflow

1. **Write it down first.** Each tool starts as a plan in its repo: the problem, the users, the data, the rules, what's
   out of scope. The AI gateway, for example, was built in two days from a ~3,900-line written spec.
2. **Make every repo readable by an agent.** Every repo has an `AGENTS.md`/`CLAUDE.md` (conventions and hard rules) and a
   `docs/HANDOFF.md` (current state, decisions, open work). Any coding session, mine or an agent's, can pick up any
   tool cold. Several sessions work in parallel on different tools, coordinated through those documents.
3. **Tests are the contract.** About 1,400 automated tests across the suite: pure rule modules unit-tested, provider
   adapters tested against recorded real responses, a call engine tested with fake Telnyx and then with real calls
   placed through headless browsers acting as phones, an AI assistant that must pass 20 golden conversations before it
   can deploy.
4. **Safety gates are code, not intentions.** Writes to outside systems start in dry-run. Customer-facing sending is off
   until an owner flips a switch. Production deploys refuse to run from a checkout that is behind GitHub, refuse to run
   if they would blank a server secret, and refuse to run from any session that isn't the owner's.
5. **Business choices are settings.** Thresholds, schedules, scripts, ring orders, scorecards: each is a setting on a
   screen with version history and restore, so changing how the business runs never needs a deploy.
6. **Verify on the real thing.** Latency is measured on real calls (and cut from about 4.3 s to 1.8 s). Phone lookups are
   timed on the server. Books are proven by reconciling to bank statements, not by trusting a report.

## Multi-agent work

For bigger builds I run coordinated agent workflows instead of one long session. My browser RPG, WYRMFALL, went from
nothing to a playable vertical slice in a day: eight parallel design agents wrote the specs, a synthesis pass froze a
single type contract, nine content agents wrote data against that contract, and an adversarial review pass found and
fixed 20 runtime bugs before release. The same pattern (parallel finders plus adversarial verifiers) produced a
378-finding audit of five years of bookkeeping, of which 135 were verified and fixed.

## Fundamentals

I keep learning the fundamentals by hand so I can read, judge and debug what agents write: Boot.dev (Level 89,
"Archsage" rank), Go and Python projects written without AI, and upstream pull requests to other people's codebases,
where the maintainers are the reviewers. See [OPEN-SOURCE.md](OPEN-SOURCE.md).
