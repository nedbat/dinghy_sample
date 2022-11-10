# Sample dinghy digests

This repo is an example of how to publish daily digests of GitHub activity with [dinghy](https://pypi.org/project/dinghy).  The sample digests some PSF projects showing [the activity in the last three days](https://nedbat.github.io/dinghy_sample/3day.html).

## Publishing your own digests

You can use this as a starting point for your own automatic publishing.

The work is done in the .github/workflows/daily-digest.yml Action.  It needs a repo secret defined: `DINGHY_ACCESS_TOKEN` is a GitHub personal access token. [Create one](https://github.com/settings/tokens) with the permissions you need.  This sample only needs `public_repo`, but you might need more depending on what information you are trying to access.

The digest itself is published using GitHub Pages.  Configure your repo to publish GitHub Pages using a custom workflow.
