# App pages

Public product, privacy, support and legal pages for Michael Kopt's applications.

Website: https://michael-kopt.github.io/app-pages/

## Ownership

This repository is the canonical source for published public pages. Application
context repositories hold store listings, screenshots and approved declaration
records, and reference these URLs instead of duplicating public policy text.
Shared tooling and release checks belong in `dev-environments`.

Both this repository and its history are public. Never commit reviewer passwords,
private endpoints, API keys, signing files or private product context.

## Publishing

GitHub Pages publishes the `docs/` directory of `main`. Static HTML/CSS needs no
dependencies or custom build workflow. `.nojekyll` disables Jekyll processing.
GitHub runs its managed Pages deployment after changes reach the publishing source.

1. Propose a change in a branch and open a PR to main.
2. Review public claims, accessibility and app-specific facts.
3. Merge approved changes and check the Pages deployment.
4. Verify affected public URLs before putting them into store metadata.

Website updates are independent of application binary releases. Record the website
commit in release evidence where policy/support content is relevant. Keep public
URLs stable and preserve redirects if a page moves. No candidate version tags or
develop/staging branches are needed for this website.

## App layout

```text
docs/
  index.html
  styles.css
  <app>/
    index.html
    privacy/index.html    # add only after review
    support/index.html    # add with a real public support destination
    terms/index.html      # when applicable
```

Auphelie's landing page is present. Privacy, support and terms pages have not yet
been published. Their intended URLs are:

- https://michael-kopt.github.io/app-pages/auphelie/privacy/
- https://michael-kopt.github.io/app-pages/auphelie/support/
- https://michael-kopt.github.io/app-pages/auphelie/terms/ (if needed)

Do not use an intended URL in store metadata until its reviewed page is live.

## Preparing an app's pages

- Verify product identity and current functionality from the app's approved context.
- Identify actual data handling, third-party services, retention and user controls.
- Obtain maintainer answers for unresolved privacy/rights questions; do not infer
  declarations from the framework or another application's policy.
- Establish a working public support contact or destination.
- Draft app-specific content, review it, then add the corresponding HTML pages.
- Add a visible effective/updated date to policies and verify all links.
- Recheck relevant public statements when the app's behavior changes.

Use relative links and shared CSS so local preview and the `/app-pages/` project
path both work. Avoid analytics, third-party fonts and external scripts by default.
Add other apps individually when their public content is ready.

## Local preview

From this directory, run `python -m http.server 8000 --directory docs`, then open
http://localhost:8000/. Review desktop/mobile layouts and keyboard navigation.
