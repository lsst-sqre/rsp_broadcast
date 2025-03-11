---
env:
  - usdfdev
enabled: true
category: info
ttl: 2w
---

Times Square is now available on the production USDF RSP. Open for details.

Times Square is now available at [https://usdf-rsp.slac.stanford.edu/times-square/](https://usdf-rsp.slac.stanford.edu/times-square/). To move your notebook repository to the production USDF RSP:

1. Install the [Times Square (USDF) GitHub App](https://github.com/apps/times-square-usdf) into your existing notebook repository. For more details, see [How to set up and install a GitHub repository into Times Square](https://rsp.lsst.io/v/usdfprod/guides/times-square/github-repos/installation-howto.html).
2. If you have GitHub branch protections set up (recommended), you will need to use the checks from Times Square USDF. For details, see [How to add GitHub branch protections to a Times Square repository](https://rsp.lsst.io/v/usdfprod/guides/times-square/github-repos/branch-protections-howto.html).

Feel free to leave your repository in the USDF development environment since we can use it for testing purposes. However, we recommend moving your usage to the USDF production RSP in the coming weeks as we start to use this environment primarily for testing new versions of Times Square.
