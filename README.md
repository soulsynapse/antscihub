# antscihub

Repository for AntSciHub materials.

[Link to the WIP](https://soulsynapse.github.io/antscihub/)

## Host the website on GitHub Pages

This repository already includes the GitHub Actions workflow at
`.github/workflows/publish.yml`. It renders the Quarto site and publishes the
generated `_site` directory whenever a commit is pushed to `main`.

1. Create a GitHub repository and push this repository to its `main` branch.
   Make sure `.github/workflows/publish.yml` is included in the push.
2. On GitHub, open the repository and go to **Settings > Pages**.
3. Under **Build and deployment**, set **Source** to **GitHub Actions**. Do not
   select a branch-based Pages source; the workflow deploys the rendered site.
4. Push a commit to `main`:

   ```bash
   git add -A
   git commit -m "Update website"
   git push origin main
   ```

5. Open the repository's **Actions** tab and select **Build and deploy Quarto
   site** to follow the first deployment. After it succeeds, the site will be
   available at `https://<owner>.github.io/<repository>/` and subsequent pushes
   to `main` will redeploy it automatically.

If GitHub Actions does not list the workflow, confirm that the workflow file is
on the repository's default branch and that Actions are enabled under
**Settings > Actions > General**.
