---
summary: Intermittent issues with catalog queries - expand for more
env:
  - idfint
  - idfprod
category: outage
enabled: true
---

Due to reasons we don't yet fully understand, certain queries are triggering a bug in Qserv, our high performance database system that hosts the DP1 catalogs. 
When this occurs, Qserv is unable to process any queries and the system requires manual intervention before queries can resume. 
We are monitoring closely to ensure minimal downtime during those events, and the Qserv team is investigating the root cause. 

We apologize for the disruption in service. 
