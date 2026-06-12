# Teachable (teachable)

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
