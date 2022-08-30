---
title: API serves outdated information
date: 2022-08-27 10:19:00
resolved: true
resolvedWhen: 2022-08-30 21:35:00
severity: disrupted
affected:
  - API
section: issue
---

**The issue has been resolved:** The expired certificate of a legacy domain has
caused the `post-publish.sh` triggered by flat-manager to exit with non-zero
exit code. This, in turn, caused flat-manager not to regenerate `appstream.xml`
used by the backend as the main data source controlling the website. Deprecated
domains were removed from the `post-publish.sh` script. {{< track "2022-08-30 21:38:00" >}}

**Connectivity issues caused the backend to serve outdated applications' metadata**

We're investigating technical issue that causes the backend to serve outadated
metadata. New applications, updates and statistics do not appear on the
website despite being available in the repository. {{< track "2022-08-30 20:11:00" >}}
