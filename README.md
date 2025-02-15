# URL-ACTION #

[![CI](
https://github.com/rzr/url-action/actions/workflows/url.yaml/badge.svg
)](
https://github.com/rzr/url-action/actions/workflows/url.yaml
)
[![CI/gh-pages](
https://github.com/rzr/url-action/actions/workflows/gh-pages.yaml/badge.svg
)](
https://github.com/rzr/url-action/actions/workflows/gh-pages.yaml
)

URL: https://github.com/rzr/url-action

Check availability of a website
useful to tell if gh-pages are enabled by running curl

For demos, check status of open PRs:

https://github.com/rzr/url-action/pulls


## URL AVAILABILITY

Usage is straightforward check sample file:

[.github/workflows/url.yaml](.github/workflows/url.yaml)

It just probe availability of URL using curl command.

if url parameter is omitted,
then by default action will check
if project has a github page online.


## GITHUB PAGES AVAILABILITY

An other more advanced recipe that attempt to deploy to gh-pages,

[.github/workflows/gh-pages.yaml](.github/workflows/gh-pages.yaml)

If URL of github-page is not available,
it is assumed that gh-pages is not enabled
then it will just bypass
and make the workflow successful.

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
- http://rzr.github.io/url-action
- https://github.com/actions/deploy-pages/issues/386#issuecomment-2660975641
- https://github.com/actions/upload-pages-artifact/issues/6#issuecomment-2660978624
