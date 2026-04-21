# pa11y-ci-action
Action to run [`pa11y-ci`](https://github.com/pa11y/pa11y-ci) for a specific website and check for accessibility problems. The workflow runs on dispatch and the user can provide the url for the site of interest. The action will run for all site's pages (provided by `sitemap.xml`). The user can provide extra arguments to include or exclude specific patterns in the urls. Check `pa11y-ci`'s documentation for extra options.

Example: pass `https://uw-echpace.github.io`.
