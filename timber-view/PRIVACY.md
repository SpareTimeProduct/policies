# Privacy Policy: TimberView

Last updated: 25 October 2026

TimberView is a Chrome extension made by SpareTimeProduct that turns a Salesforce
debug log into an interactive tree. It runs entirely on your device. We do not
operate any server that TimberView talks to, and we receive no data from it.

TimberView is an independent tool. It is not affiliated with, endorsed by or
sponsored by Salesforce.

## What TimberView accesses

- **Salesforce debug log content.** On supported Salesforce pages the extension
  checks, locally in your browser, whether the page is a debug log. If you click
  "View in TimberView", it reads the log text either from the page itself or by
  fetching it from your Salesforce org's own log download address (`/servlet/servlet.FileDownload`) using
  your existing browser session. If you open a saved log file in the viewer, the
  file is read in your browser and never uploaded.
- **Nothing else.** It does not read your Salesforce records, your credentials,
  your cookies (the browser attaches your session to the request to your own org),
  your browsing history, or any page outside the Salesforce domains listed below.

## How that data is used

- To hand a log from the Salesforce page to the viewer tab, the log text is
  written to `chrome.storage.local` (local browser storage on your device only)
  under a one-time random key.
- The viewer reads and deletes that entry as soon as it loads. If the viewer
  never opens, any leftover entry is deleted the next time the browser starts or
  the extension is installed or updated.
- All parsing and rendering happens locally in your browser. The code, the fonts
  and the jsTree and jQuery libraries are bundled with the extension.
- Your theme choice (light or dark) is saved in the viewer page's local storage.

## What TimberView does not do

- It does not send log content, page content or any other data to us or to any
  third party.
- It does not use analytics, tracking, advertising or error-reporting services.
- It does not load code or fonts from the network.
- It does not sell or share data, and it does not use data for anything other
  than showing you the log you asked to see.
- The only network request it makes is the optional fetch of a debug log from
  your own Salesforce org's domain, using your existing session. That request
  stays between your browser and Salesforce.

## Data retention

No log data is retained. Closing the viewer tab discards the parsed tree. The
only thing TimberView persists is your theme preference.

## Permissions

- **Host access** to Salesforce org domains (`*.my.salesforce.com`,
  `*.lightning.force.com`, `*.salesforce-setup.com`, `*.vf.force.com`,
  `*.visualforce.com`): to detect debug log pages, show the button, and fetch a
  log from your org when you ask.
- **storage / unlimitedStorage**: to pass a log (which can be up to 20 MB) from
  the page to the viewer tab. Chrome's default storage quota is smaller than
  Salesforce's maximum log size.

## Changes to this policy

If the way TimberView handles data ever changes, this page will be updated
and the date above changed before the new version is released.

## Contact

Questions about this policy: sparetimeproduct@gmail.com
