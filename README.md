# URL-ACTION #

[![CI](
https://github.com/rzr/url-action/actions/workflows/url.yml/badge.svg
)](
https://github.com/rzr/url-action/actions/workflows/url.yml
)

URL: https://github.com/rzr/url-action

Check availability of a website
useful to tell if gh-pages are enabled by running curl

Usage is straightforward check sample file:

[.github/workflows/url.yml](.github/workflows/url.yml)

if url parameter is omitted,
then by default action will check
if project has a github page online.



For the record i made it to prevent deploying to gh-pages,
when forking projects that have this feature enabled.

Typical observed issue when using actions/deploy-pages@v4

```
Fetching artifact metadata for "github-pages" in this workflow run
Found 3 artifact(s)
Creating Pages deployment with payload:
(...)
Error: Creating Pages deployment failed
Error: HttpError: Not Found
(...)
Error: Error: Failed to create deployment (status: 404) with build version BADC0DE. Request ID ...
Ensure GitHub Pages has been enabled: https://github.com/.../.../settings/pages
```


## RESOURCES ##

- https://github.com/marketplace/actions/url-action
