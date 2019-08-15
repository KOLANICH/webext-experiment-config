about:config WebExtensions API experiment [![Unlicensed work](https://raw.githubusercontent.com/unlicense/unlicense.org/master/static/favicon.png)](https://unlicense.org/)
=========================================

This repo contains a pair of extensions and one demo webapp.
* `experiment` directory contains the source of the [experimental WebExtensions API](https://firefox-source-docs.mozilla.org/toolkit/components/extensions/webextensions/index.html) for passing some API for editing [`about:config`](about:config) prefs into WebExtensions. **Install it first.** [`nightly.link`](https://nightly.link/KOLANICH/webext-experiment-config/workflows/CI/master/experiment.xpi)
* For `arkenfox` addon you will also need a yet another WebExtension experiment, [`experiment.parse`](https://github.com/KOLANICH/webext-experiment-parse/tree/master/experiment) ([`nightly.link`](https://nightly.link/KOLANICH/webext-experiment-parse/workflows/CI/master/experiment.xpi)), that allows to use native JavaScript parser built-into Firefox. Works faster and more correctly than a JS-based surrogate for it we have. If you don't want it, just remove the permission from `manifest.json` and the addon will use the regexp-based surrogate.
* [`arkenfox` directory](./unlocker) contains a simple extension checking prefs against [arkenfox user.js](https://github.com/arkenfox/user.js) - a privacy-preserving preset for `about:config`. If there are differences, they can be easily fixed. [`nightly.link`](https://nightly.link/KOLANICH/webext-experiment-config/workflows/CI/master/arkenfox.xpi)
* [`unlocker` directory](https://github.com/KOLANICH/webext-experiment-config/tree/master/unlocker) contains a simple extension just unlocking all the locked prefs in `about:config`. [`nightly.link`](https://nightly.link/KOLANICH/webext-experiment-config/workflows/CI/master/unlocker.xpi)

Note: WebExtension Experiments support in Firefox other than Nightly is damn bad and changes.

For the docs see [the schema](./experiment/schema.json) .
