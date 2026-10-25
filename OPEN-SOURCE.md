# Open source and learning

## Merged upstream contributions

19 pull requests merged into 4 outside projects (checked October 24, 2026).

| Project | Pull request | Merged |
|---|---|---|
| [apache/iceberg-python](https://github.com/apache/iceberg-python) (Apache Software Foundation) | [#3893](https://github.com/apache/iceberg-python/pull/3893): correct LICENSE paths for wheels and document the bundled Cython runtime | Sep 11, 2026 |
| [apache/maka](https://github.com/apache/maka) (Apache Incubator, local-first AI agent workspace) | [#4438](https://github.com/apache/maka/pull/4438): keep MCP text clipping from splitting UTF-16 surrogate pairs (with the issue that reported it) | Sep 3, 2026 |
| [studie-tech/TheNinjaRPG](https://github.com/studie-tech/TheNinjaRPG) | [#1573](https://github.com/studie-tech/TheNinjaRPG/pull/1573): stop a countdown firing up to a second early (diagnosed a client/server rounding mismatch) | Sep 20, 2026 |
| [securo-finance/securo](https://github.com/securo-finance/securo) (self-hosted personal finance, ~4,100 stars) | 16 merged: [#798](https://github.com/securo-finance/securo/pull/798) honor the number-format setting in amount input; [#1192](https://github.com/securo-finance/securo/pull/1192) count a shared credit line once in net worth; [#1197](https://github.com/securo-finance/securo/pull/1197) hold a card's limit for future-dated charges; [#1198](https://github.com/securo-finance/securo/pull/1198) compute group balances from who actually paid; [#1199](https://github.com/securo-finance/securo/pull/1199) don't report a slow bank import as a failed connection; [#1168](https://github.com/securo-finance/securo/pull/1168) let Generate Pending cover schedules with auto-generate off; [#1167](https://github.com/securo-finance/securo/pull/1167) show a holding's transaction total in its own currency; [#1226](https://github.com/securo-finance/securo/pull/1226) keep the opening balance date when editing an account; [#1227](https://github.com/securo-finance/securo/pull/1227) a System theme that follows the OS; [#1193](https://github.com/securo-finance/securo/pull/1193) stop podman-compose appending "}" to a URL; and currency support for MYR, CNY, SAR, QAR, JMD, MKD and ZAR ([#939](https://github.com/securo-finance/securo/pull/939), [#940](https://github.com/securo-finance/securo/pull/940), [#950](https://github.com/securo-finance/securo/pull/950), [#951](https://github.com/securo-finance/securo/pull/951), [#1166](https://github.com/securo-finance/securo/pull/1166), [#1225](https://github.com/securo-finance/securo/pull/1225)) | Sep 3 to Oct 22, 2026 |

Open: four pull requests to [omarchy](https://github.com/omacom/omarchy) (per-app volume sliders, SSH key removal for the
invoking user, Chromium first-run preferences, keeping removed preinstalls removed).

## Public projects

| Repo | What it is |
|---|---|
| [gator](https://github.com/shaynhornik/gator) | Terminal RSS aggregator in Go: users, feeds, follows and a background scraper on Postgres, with goose migrations and sqlc-generated queries |
| [pokedexcli](https://github.com/shaynhornik/pokedexcli) | REPL Pokédex in Go with a paginated API client and a TTL cache reaped by a goroutine, with unit tests |
| [cli-pokemon-game](https://github.com/shaynhornik/cli-pokemon-game) | Turn-based battle game in the terminal (type chart, moves, routes). Written by hand with no AI or autocomplete, on purpose |
| [static_site](https://github.com/shaynhornik/static_site) | Static site generator: Markdown to an HTML node tree to pages, with inline and block parsers and unit tests |
| [portfolio_site_generator](https://github.com/shaynhornik/portfolio_site_generator) | CLI that builds a static portfolio site from any GitHub user's public data, with one-command GitHub Pages deploy |
| [github_profile_readme_generator](https://github.com/shaynhornik/github_profile_readme_generator) | Zero-dependency CLI that generates a profile README from the GitHub REST API |
| [chirpy](https://github.com/shaynhornik/chirpy) | HTTP server in Go: JSON API, JWT access tokens with refresh and revoke, Argon2id password hashing, Postgres with sqlc and goose, a payment webhook checked by API key |
| [Astroids](https://github.com/shaynhornik/Astroids) · [bookbot](https://github.com/shaynhornik/bookbot) | Early Boot.dev projects (Pygame Asteroids clone, text statistics) |

## Learning path

Boot.dev since May 2025, working through the back-end path (Python, data structures and algorithms, Linux, Git, SQL, Go, HTTP clients and servers in Go, file servers and CDNs on S3 and CloudFront, memory management in C, and an AI agent in Python). The public repos above are the trail: Python fundamentals, Git, an AI coding agent, a static site generator, a hand-written terminal game, then Go, Postgres and HTTP servers.
