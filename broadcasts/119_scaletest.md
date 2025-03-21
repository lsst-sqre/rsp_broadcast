---
enabled: true
summary: |
  Scaletesting ongoing 12:30-15:30 PT - consider doing something else
env:
  - idfint
timezone: America/Los Angeles
ttl: 3hr
rules:
  - freq: weekly
    start: 2025-01-23T12:30
    by_weekday:
      - day: friday
---

SQuaRE is stress-testing data-int.
This may degrade or even interrupt normal service.

You are welcome to continue using the cluster during this time if you want, but it might be a miserable if not pointless experience.
