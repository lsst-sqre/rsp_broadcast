---
enabled: true
summary: |
  This is a test of a scheduled message.
env:
  - idfdev
timezone: America/Los Angeles
ttl: 10min
rules:
  - freq: weekly
    start: 2021-08-12T14:35
    by_weekday:
      - day: thursday
---

Test content.
