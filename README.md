# Queen's University Belfast (queens-university-belfast)

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

Queen's University Belfast is a public, research-intensive Russell Group university in Belfast,
Northern Ireland, founded in 1845. This repository catalogs the institution's public,
machine-readable footprint as an [APIs.json](http://apisjson.org) profile.

**Read the operator column before you read anything else.** A university is a federation of buyers,
not a producer, and most of what looks like a QUB API is a vendor's product running under a QUB
hostname. This profile was re-run on 2026-08-30 under the API Evangelist university pipeline, which
settles *who operates the thing* before it saves any contract.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/queens-university-belfast/refs/heads/main/apis.yml
- Run with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=queens-university-belfast-api-evangelist&utm_content=repo

## Type

- Type: Index (`x-type: university`)
- Category: Public Research University
- Position: Consumer
- Access: 3rd-Party

## Tags

University, Higher Education, Education, Research, United Kingdom, Northern Ireland, Russell Group,
Identity Federation, Research Repository, Open Access, OAI-PMH, Shibboleth, SAML, Research Computing

## Surfaces, by operator

| Surface | Operator | Evidence |
|---|---|---|
| Shibboleth SAML 2.0 Identity Provider, `https://qub.ac.uk/shibboleth` | **institution** | Registered in the UK Access Management Federation; signed entity descriptor resolvable via MDQ (200); scope `qub.ac.uk`; SSO on `qub-shib.qub.ac.uk` |
| DataCite repository client `BL.QUB` (since 2015) | **institution** | `api.datacite.org/clients/bl.qub` → 200; QUB is DataCite consortium organization `jxtg` |
| Research Portal OAI-PMH, `pureadmin.qub.ac.uk/ws/oai` | tenant | `?verb=Identify` → 200, repositoryName "QUB Research Portal"; host CNAMEs to `qub-pva.elsevierpure.com` |
| Pure Web Service API, `pureadmin.qub.ac.uk/ws/api` | tenant | Served OpenAPI is titled "Pure API", contact `pure-support@elsevier.com`, version 5.36.2-1; anonymous call → 401 |
| Canvas LMS, `canvas.qub.ac.uk/api/v1` | tenant | CNAMEs to `qub-vanity.instructure.com`; `/api/v1/courses` → 401; LTI 1.3 JWKS → 200 |
| Ex Libris Primo discovery, `qub.primo.exlibrisgroup.com` | tenant (pointer only) | `vid=44QSUB_INST:QUB` → 200 |

## Domain standard conformance (Kin Score `education` regime)

Probed live on 2026-08-30 and recorded in
[conformance/queens-university-belfast-conformance.yml](conformance/queens-university-belfast-conformance.yml):

- `shibboleth`, `saml` — conformant, **institution-operated**
- `oai-pmh` — conformant, tenant deployment
- `datacite` — conformant, institution registration
- `lti` — conformant, tenant deployment (Canvas LTI 1.3 JWKS)
- `crossref` — partial (School of Law is a Crossref member, prefix `10.53386`; no institution-wide member record found)
- `scim`, `orcid`, `oneroster`, `ed-fi`, `caliper`, `qti` — probed for, not found

## Plans / Rate Limits / FinOps / Security

- Plans: [plans/queens-university-belfast-plans-pricing.yml](plans/queens-university-belfast-plans-pricing.yml)
- Rate Limits: [rate-limits/queens-university-belfast-rate-limits.yml](rate-limits/queens-university-belfast-rate-limits.yml)
- FinOps: [finops/queens-university-belfast-finops.yml](finops/queens-university-belfast-finops.yml)
- Domain security: [security/queens-university-belfast-domain-security.yml](security/queens-university-belfast-domain-security.yml)

## Timestamps

- Created: 2026-06-03
- Modified: 2026-08-30

## Common Properties

- Website: https://www.qub.ac.uk/
- Research repository: https://pure.qub.ac.uk/
- Identity federation: http://mdq.ukfederation.org.uk/entities/https%3A%2F%2Fqub.ac.uk%2Fshibboleth
- Library catalog: https://qub.primo.exlibrisgroup.com/discovery/search?vid=44QSUB_INST:QUB
- Course catalog: https://www.qub.ac.uk/courses/
- Research computing: https://www.ni-hpc.ac.uk/
- AI policy: https://blogs.qub.ac.uk/digitallearning/ai/ai-in-research/qub-guidance-on-responsible-use-of-ai-in-research/
- AI tooling: https://libguides.qub.ac.uk/AILibrary
- Privacy: https://www.qub.ac.uk/about/website/privacy-and-cookies/
- Support: https://www.qub.ac.uk/contact/ask-a-question/
- LinkedIn: https://www.linkedin.com/school/queens-university-belfast/
- Review: [review.yml](review.yml)

## What changed on 2026-08-30, and why the score should fall

The June 2026 profile of this institution held **38 OpenAPI documents** — 37 refined per-tag specs
plus the pristine source — and 89 artifacts derived from them (Postman and OpenCollection
collections, JSON Schemas, JSON Structures, examples, a vocabulary, a JSON-LD context, an
authentication summary, an agentic-access classification, two Spectral rulesets). **Every one of
those documents was Elsevier's contract, not Queen's.** Each carried `info.title: "Pure API"` or
`"Pure activity … API"` and `info.contact.email: pure-support@elsevier.com`; the same titles ship in
nine other university repositories in this catalog.

A hostname check could not see it: `pure.qub.ac.uk` and `pureadmin.qub.ac.uk` sit under the
university's own registrable domain, so a host-based verdict reads them as institution-owned. DNS
settles it — both CNAME to `qub-pva.elsevierpure.com` → `eu.prod.elsevierpure.com`. This is the
`scholarbank.nus.edu.sg` pattern: a vanity hostname on a vendor's platform.

All 127 files were removed, the tenancies were recorded as relationships instead, and the surfaces
Queen's genuinely operates — its federated identity provider and its DataCite registration — were
found and recorded with live evidence. Fewer artifacts, correctly attributed, is the point. A lower
composite score here is the pipeline working, not a regression.

## Notes

- No `api.qub.ac.uk`, `developer.qub.ac.uk`, `data.qub.ac.uk` or `opendata.qub.ac.uk` host resolves.
- No `llms.txt` and no `/.well-known/security.txt` on `www.qub.ac.uk` (both 404).
- The "Qmulus" open data API (`qmulus.io`) that search engines surface for "Queen's University Open
  Data API" belongs to Queen's University at Kingston, **Ontario** — not Queen's University
  **Belfast**. It is deliberately excluded.
- No official university-wide GitHub organization was confirmed. The `qub` and `qub-ac-uk` GitHub
  accounts are personal user accounts with no name, bio, or website tying them to the university,
  and the QUB-branded orgs that exist (`DIPSA-QUB`, `QUB-Genomics-CTU`, `QUB-AI`, and similar) are
  research groups and schools. No `GitHubOrganization` pointer is asserted.
- QUB additionally operates federated identity for two other Northern Ireland organisations under
  its own domain: the Healthcare Library of Northern Ireland (`honni.qub.ac.uk`) and the Agri-Food
  and Biosciences Institute (`afbi.qub.ac.uk`).
- `www.ni-hpc.ac.uk` (the NI-HPC centre and the Kelvin2 system) CNAMEs to QUB's own Terminalfour CMS
  instance, which is why it is recorded as an institution-operated research-computing pointer.

## Maintainers

- Kin Lane — kin@apievangelist.com
