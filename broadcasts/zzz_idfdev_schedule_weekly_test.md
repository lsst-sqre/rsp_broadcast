---
enabled: false
summary: |
  This is a test of a message that appears weekly at 15:20 project.
env:
  - idfdev
timezone: America/Los Angeles
ttl: 10min
rules:
  - freq: weekly
    start: 2021-08-12T15:20
    by_weekday:
      - day: thursday
---
