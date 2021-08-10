# Broadcast messages for the Rubin Science Platform

This repository contains the content source for broadcast messages of all RSP environments managed by [Phalanx](https://github.com/lsst-sqre/phalanx).
A *broadcast* is a message that appears to all RSP users, and may be visible to anonymous users on the RSP's homepage ([Squareone](https://github.com/lsst-sqre/squareone)) as well.
These broadcasts are the content seen in the red ribbon at the top of the home page, for instance.

Broadcasts are individual Markdown files in the [`broadcasts/`](./broadcasts) directory.
Once you commit or merge to the default branch (`main`), broadcasts are refreshed automatically in each RSP environment through the [Semaphore](https://github.com/lsst-sqre/semaphore) service.
