---
title: API Reference

language_tabs:

toc_footers:
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes:
  - auth
  - organizations
  - users
  - policies
  - rules
  - projects
  - revisions
  - builds
  - licenses

search: true
---

# Introduction

Welcome to the FOSSA API! Each project analyzed by FOSSA exposes a REST API for
custom integration with CI, scripts, and client applications.

The public FOSSA API is available at `https://api.fossa.io/`. If you are
integrating with an on-premises installation, substitute the hostname of your
on-premises installation for `api.fossa.io`.

Code examples use `http` from [HTTPie](https://httpie.org/).

<aside class="warning">
The FOSSA API is currently in alpha. Some endpoints may cause poor performance and system instability if called with malformed parameters. As a best practice, you should always paginate responses to avoid potentially poor performance.
</aside>
