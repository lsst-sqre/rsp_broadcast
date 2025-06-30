---
enabled: true
summary: |
  [Patch Thursday](https://rsp.lsst.io/guides/life/patch-thursday.html) is **happening now,** 3pm–5pm Pacific / 22:00–00:00 UT.
env:
  - idfdev
  - idfint
  - idfprod
  - usdfdev
  - usdfint
  - usdfprod
timezone: America/Los Angeles
ttl: 2hr
rules:
  - freq: weekly
    start: 2021-08-11T15:00
    by_weekday:
      - day: thursday
---

On most Thursday afternoons we deploy updates and perform routine maintenance actions on the Rubin Science Platform.

This is not a outage period and you do not need to stop using the Platform.

However there might be transient service interruptions or instabilities during this time, and very rarely an update can take longer than anticipated because of issues not seen in testing.
**If you are using the RSP during this time, save your work early and often** as on rare occasions user sessions may need to be terminated.
Wait until after this window to [file bug reports](https://data.lsst.cloud/support) (if you still see a problem).

For more information about Patch Thursday, [see our post on the Community forum](https://rsp.lsst.io/guides/life/patch-thursday.html).
