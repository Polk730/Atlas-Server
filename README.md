# Atlas Web

The Atlas interface on GitHub Pages, connected to the owner's Atlas server at
**https://atlasbyoliver.com**. GitHub does not run the language model.

## Publish

In this repository, open **Settings → Pages → Source → GitHub Actions**.
Then open **Actions → Publish Atlas UI → Run workflow**.
The expected address is **https://polk730.github.io/Atlas-Server/**.

Install the separate GitHub Pages compatibility update on the Atlas server PC
before using the page. The server explicitly permits only
`https://polk730.github.io`; it does not allow arbitrary websites.

## Repository contents

- `site.zip`: the static HTML, CSS, JavaScript and public image assets.
- `.github/workflows/pages.yml`: publishes the archive through GitHub Pages.

To edit the interface, extract `site.zip`, edit its contents, and recreate the
archive with `index.html` at its root. No build dependencies are required.

## Data and sessions

Model files, server-side account credentials, private user data and access keys
are not included. Account login and AI requests go directly over HTTPS to the
Atlas server, not to GitHub. Pages uses a session-scoped bearer credential
instead of third-party cookies. Sessions expire after eight hours; a server
restart may require signing in again. Both browser storage and cloud account
data are still separated by account.

The server must stay online. Large cutscenes, math vendor libraries and music
remain on the Atlas server to avoid duplicating them in the repository.

The deployment contains the current games, local multiplayer, seasonal
backgrounds, and friends/message notifications. Background notifications still
require an open page; GitHub Pages does not add an offline push service.