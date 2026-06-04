# Queen's University Belfast (queens-university-belfast)

Queen's University Belfast is a Russell Group research-intensive university in Northern Ireland, United Kingdom, founded in 1845 and ranked #206 in the QS World University Rankings 2025. This repository catalogs the institution's public, machine-readable developer/API footprint as an [APIs.json](http://apisjson.org) profile. That footprint is limited and research-centric: the primary confirmed open interface is the Pure-based Research Portal's OAI-PMH metadata endpoint.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/queens-university-belfast/refs/heads/main/apis.yml
- Run with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=queens-university-belfast-api-evangelist&utm_content=repo

## Type

- Type: Index
- Position: Consumer
- Access: 3rd-Party

## Tags

Education, Higher Education, University, Research, Open Access, OAI-PMH, United Kingdom, Northern Ireland

## APIs

- **Queen's University Belfast Research Portal (Pure OAI-PMH)** — OAI-PMH metadata harvesting endpoint for the institutional research repository (Elsevier Pure), exposing research outputs, datasets, and theses.
  - Base URL: `https://pureadmin.qub.ac.uk/ws/oai`
  - Human URL: https://pure.qub.ac.uk/
  - Protocol docs: https://www.openarchives.org/OAI/openarchivesprotocol.html

## Plans / Rate Limits / FinOps

- Plans: [plans/queens-university-belfast-plans-pricing.yml](plans/queens-university-belfast-plans-pricing.yml)
- Rate Limits: [rate-limits/queens-university-belfast-rate-limits.yml](rate-limits/queens-university-belfast-rate-limits.yml)
- FinOps: [finops/queens-university-belfast-finops.yml](finops/queens-university-belfast-finops.yml)

## Timestamps

- Created: 2026-06-03
- Modified: 2026-06-03

## Common Properties

- Website: https://www.qub.ac.uk/
- Research Portal: https://pure.qub.ac.uk/
- LinkedIn: https://www.linkedin.com/school/queen's-university-belfast/
- Review: [review.yml](review.yml)

## Notes

- All entries reflect URLs verified during research on 2026-06-03; no endpoints were fabricated.
- The OAI-PMH endpoint was confirmed live (`ListMetadataFormats` returns valid OAI-PMH XML); the bare `Identify` verb returned HTTP 500 on this Pure instance, while other verbs and the base endpoint return 200.
- No dedicated developer portal, open REST API catalog, or API key/sign-up flow was found.
- The "Qmulus" open data API found in search belongs to Queen's University in **Canada**, not Queen's University **Belfast**, and was deliberately excluded.
- No official university-wide GitHub organization was confirmed (only department/research-group accounts such as DIPSA-QUB), so no GitHub common property is asserted.

## Maintainers

- Kin Lane — kin@apievangelist.com
