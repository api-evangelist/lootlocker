# LootLocker (lootlocker)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

LootLocker is a game backend-as-a-service platform that provides a REST API for building cross-platform game features without managing server infrastructure. The platform covers player authentication across Steam, Epic Games, PlayStation, Xbox, Nintendo Switch, Apple, Google, and custom white-label flows, as well as leaderboards, player progressions, virtual economies, persistent storage, cloud saves, and player file hosting. Developers can also access character systems, asset management, in-app purchasing, missions, collectibles, and Twitch Drops integration through a unified API surface. SDKs are available for Unity, Unreal Engine, and Godot, with basic integration support for GameMaker, Construct 3, and GDevelop.

**APIs.json:** https://raw.githubusercontent.com/api-evangelist/lootlocker/refs/heads/main/apis.yml

**Naftiko:** https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=lootlocker-api-evangelist&utm_content=repo

---

## Tags

Games, Game Backend, Game Backend as a Service, Player Authentication, Leaderboards, Progressions, Virtual Economy, Cloud Save, Cross-Platform, Multiplayer

---

## APIs

| Name | Description | Reference |
|------|-------------|-----------|
| LootLocker Game API | Client-side API integrated into game builds for player sessions, inventory, leaderboards, progressions, storage, and more | https://ref.lootlocker.com/game-api/ |
| LootLocker Server API | Trusted server-side API for secure communication between dedicated game servers and the LootLocker backend | https://ref.lootlocker.com/server-api/ |
| LootLocker Admin API | Platform management API for game editor integrations and backend configuration tooling | https://ref.lootlocker.com/admin-api/ |

---

## Plans / Rate Limits / FinOps

| Resource | File |
|----------|------|
| Plans and Pricing | [plans/lootlocker-plans-pricing.yml](plans/lootlocker-plans-pricing.yml) |
| Rate Limits | [rate-limits/lootlocker-rate-limits.yml](rate-limits/lootlocker-rate-limits.yml) |
| FinOps | [finops/lootlocker-finops.yml](finops/lootlocker-finops.yml) |

**Plan summary:** Trial (free, 1,000 MAU/month), Non-Commercial License (free for non-monetized games), Developer (custom pricing, adds console auth), Publisher (custom pricing, unified player accounts, Twitch Drops, $0.015/MAU overage).

---

## Timestamps

| Field | Value |
|-------|-------|
| Created | 2026-06-12 |
| Modified | 2026-06-12 |

---

## Common

| Type | URL |
|------|-----|
| Website | https://lootlocker.com/ |
| Documentation | https://docs.lootlocker.com/ |
| GitHub Org | https://github.com/lootlocker |
| LinkedIn | https://www.linkedin.com/company/lootlocker |
| Blog | https://lootlocker.com/blog |
| Pricing | https://lootlocker.com/pricing |
| Status Page | https://status.lootlocker.com/ |
| X | https://x.com/mylootlocker |
| Changelog | https://lootlocker.com/changelog |
| SDKs | https://lootlocker.com/sdk |

---

## Maintainers

| Name | Email |
|------|-------|
| Kin Lane | kin@apievangelist.com |
