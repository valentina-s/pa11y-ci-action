# pa11y-ci-action
Action to run [`pa11y-ci`](https://github.com/pa11y/pa11y-ci) for a specific website and check for accessibility problems. The workflow runs on manual dispatch and the user can provide the url for the site of interest. Currently, the there are two workflow options:

1. Single Page: [`.github/workflows/run_pa11y-ci_page.yml`](https://github.com/valentina-s/pa11y-ci-action/blob/main/.github/workflows/run_pa11y-ci_page.yml)

2. Whole Website: [`.github/workflows/run_pa11y-ci_site.yml`](https://github.com/valentina-s/pa11y-ci-action/blob/main/.github/workflows/run_pa11y-ci_site.yml)

Note, the second option expects the site to have a `sitemap.xml`. One can test this by check if `[url]/sitemap.xml` is a valid url. The action will run for all site's pages provided in the list. The user can provide extra arguments to include or exclude specific patterns in the urls. If such map does not exist one can separately first extract a list of urls with the url as a root, and then pass the list to the `pa11y-ci` command. Check `pa11y-ci`'s documentation for extra options.


To run `pa11y-ci`:
1. Fork the repo.
1. Go to Actions (top tabs).
2. In the left panel Workflows, click on the corresponding `.yml` file.
3. Click `Run workflow` and pass the url as an argument, e.g. `https://uw-echospace.github.io`.

   <img width="1479" height="712" alt="Screenshot 2026-06-04 at 1 30 02 PM" src="https://github.com/user-attachments/assets/20ced9ab-e58c-471b-a7a5-efd7bb58b724" />

If people can also adapt these workflows to set up a regularly scheduled GitHub Action to check their website.

   
