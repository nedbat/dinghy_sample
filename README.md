# Sample dinghy digests

This repo is an example of how to publish daily digests of GitHub activity with [dinghy](https://pypi.org/project/dinghy).  The sample digests some PSF projects showing [the activity in the last three days](https://nedbat.github.io/dinghy_sample/3day.html).

## Publishing your own digests

You can use this as a starting point for your own automatic publishing.

The work is done in the .github/workflows/daily-digest.yml Action.  It needs two repo secrets defined:

- `DINGHY_ACCESS_TOKEN` is a GitHub personal access token. [Create one](https://github.com/settings/tokens) with the permissions you need.

- `DIGESTER_EMAIL` is the email address to use as the author of the commits that add the digest each day.

You will need a `digests` branch.  Create one from `main`.  The action will update this branch with digest content.

The digest itself is published using GitHub Pages.  Configure your repo to publish the root directory from the `digests` branch.
