# Teachable (teachable)

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Teachable is an online course and coaching platform that empowers creators to build and sell educational content without technical expertise. The Teachable REST API provides programmatic access to school management capabilities including course management, user enrollment, quiz responses, and sales transaction data. The API supports two authentication patterns: a server-side Admin API using API keys and an OAuth API for third-party application integrations. API access is available on Growth and Advanced plans, with webhook support for event-driven workflows covering enrollment, lecture completion, sales, and user lifecycle events.

- **APIs.json**: [https://raw.githubusercontent.com/api-evangelist/teachable/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/teachable/refs/heads/main/apis.yml)
- **Naftiko**: [https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=teachable-api-evangelist&utm_content=repo](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=teachable-api-evangelist&utm_content=repo)

## Tags

Online Courses, E-Learning, Education, Course Management, Enrollments, Coaching, Memberships, Transactions

## APIs

### Teachable Admin API

REST API for managing Teachable school data including courses, users, enrollments, quiz responses, pricing plans, transactions, and webhooks. Authenticated via API key header and available on Growth plan and above.

- **Base URL**: https://developers.teachable.com/v1
- **Documentation**: https://docs.teachable.com/docs/overview-1
- **Reference**: https://docs.teachable.com/reference/listcourses

**Key Endpoints:**

| Resource | Method | Path |
|---|---|---|
| Courses | GET | /v1/courses |
| Course | GET | /v1/courses/{course_id} |
| Course Enrollments | GET | /v1/courses/{course_id}/enrollments |
| Course Progress | GET | /v1/courses/{course_id}/progress |
| Lectures | GET | /v1/courses/{course_id}/lectures/{lecture_id} |
| Quizzes | GET | /v1/courses/{course_id}/lectures/{lecture_id}/quizzes |
| Users | GET/POST | /v1/users |
| Enroll | POST | /v1/enroll |
| Unenroll | POST | /v1/unenroll |
| Pricing Plans | GET | /v1/pricing_plans |
| Transactions | GET | /v1/transactions |
| Webhooks | GET | /v1/webhooks |

### Teachable OAuth API

OAuth 2.0-based API enabling third-party applications to authenticate on behalf of Teachable school owners with token refresh and revocation support.

- **Documentation**: https://docs.teachable.com/docs/overview-1

## Plans / Rate Limits / FinOps

| Resource | File |
|---|---|
| Plans & Pricing | [plans/teachable-plans-pricing.yml](plans/teachable-plans-pricing.yml) |
| Rate Limits | [rate-limits/teachable-rate-limits.yml](rate-limits/teachable-rate-limits.yml) |
| FinOps | [finops/teachable-finops.yml](finops/teachable-finops.yml) |

**Plan Summary:**

| Plan | Monthly | Annual | Transaction Fee | API Requests/Mo |
|---|---|---|---|---|
| Starter | $39 | $29 | 7.5% | None |
| Builder | $89 | $69 | 0% | None |
| Growth | $189 | $139 | 0% | 10,000 |
| Advanced | $399 | $309 | 0% | 25,000 |
| Unlimited | Custom | Custom | 0% | Custom |

**Rate Limits:** 100 requests per minute per school. HTTP 429 on exceeded limit with `RateLimit-Limit`, `RateLimit-Remaining`, and `RateLimit-Reset` response headers.

## Timestamps

- **Created**: 2026-06-12
- **Modified**: 2026-06-12

## Common Properties

| Type | URL |
|---|---|
| Website | https://teachable.com |
| Documentation | https://docs.teachable.com |
| GitHub Organization | https://github.com/usefedora |
| LinkedIn | https://www.linkedin.com/company/teachable |
| X | https://x.com/teachable |
| Blog | https://www.teachable.com/blog |
| Changelog | https://changelog.teachable.com |
| Pricing | https://teachable.com/pricing |
| Status Page | https://www.teachablestatus.com |
| Support | https://support.teachable.com |

## Maintainers

- **Kin Lane** - kin@apievangelist.com
