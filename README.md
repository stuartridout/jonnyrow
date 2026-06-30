# Jonny's Row Tracker

A self-contained web page built in Claude Design, hosted on GitHub Pages.

## Live site

Once GitHub Pages is enabled (see below), the page is served at:

**https://stuartridout.github.io/jonnyrow/**

## How it works

`index.html` is a fully self-contained bundle: fonts, images, and the
JavaScript app are all embedded directly in the file (base64-encoded, gzip
compressed). When the page loads, it unpacks those assets in the browser and
renders the app — there is no build step.

At runtime the page pulls its data from a published Google Sheet via the
Google Visualization CSV endpoint
(`https://docs.google.com/spreadsheets/d/<id>/gviz/tq?tqx=out:csv&sheet=Sheet1`).
For the live data to show up, that sheet must remain shared so that anyone
with the link can view it.

## Enabling GitHub Pages

This page serves as plain static HTML, so no build or workflow is required:

1. Go to the repository's **Settings → Pages**.
2. Under **Build and deployment → Source**, choose **Deploy from a branch**.
3. Pick the branch that holds this file and the `/ (root)` folder, then
   **Save**.
4. Wait ~1 minute and open the live URL above.

The `.nojekyll` file tells GitHub Pages to serve the files as-is rather than
running them through Jekyll.

## Editing

The page was designed in Claude Design. To change it, re-export from Claude
Design and replace `index.html`.
