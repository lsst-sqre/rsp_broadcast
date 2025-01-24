---
enabled: true
category: info
summary: |
  Heads up: Scaletesting today 12:30 PT for ~ 2 hours, services may be severely degraded
env:
  - idfint
timezone: America/Los Angeles
ttl: 12hr
rules:
  - freq: weekly
    start: 2025-01-23T00:30
    by_weekday:
      - day: friday
---

SQuaRE is conducting a scale-testing campaign on data-int.
Weekly stress tests on Friday afternoons may degrade or even interrupt normal service.

You are welcome to continue using the cluster during this time if you want, but it might be a miserable if not pointless experience.
