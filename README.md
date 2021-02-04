# GQL Foundation website

This site is built using [Hugo](https://gohugo.io) and hosted on [Netlify](https://netlify.com).

## Running the site locally {#running}

To run the site locally, you must first set it up:

1. [Install Hugo](https://gohugo.io/getting-started/installing/). For this site, you need to install an "extended" version of Hugo with support for [Sass](https://sass-lang.com).
1. Install [Yarn](https://classic.yarnpkg.com/en/docs/getting-started), and run `yarn` to install dependencies

Now you can launch a development web server:

```shell
make serve
```

Navigate to http://localhost:1313 in your browser to view the site.

## Publishing the site

This site is published automatically by Netlify. Any time you push changes to the `master` branch, the site will be rebuilt and republished with those changes.

## Updating the site's content

All of the site's content is generated from sources that are not directly in the HTML templates:

* The site's title is set using the `title` variable in the site's main [`config.toml`](config.toml) configuration file; the subtitle is set using `params.home.subtitle`; the large-text info section above the "About" section is set using `params.home.info`; and the "About" section is set using `params.home.about`. Markdown is supported in *all* of these text blocks.
* The navbar links are generated from the `params.nav` map in [`config.toml`](config.toml)
* The FAQ is generated from the [`data/faq.yaml`](data/faq.yaml) file

## Aesthetic

This site uses the [Bulma](https://bulma.io) CSS framework. The Sass used to build the site's CSS is in [`assets/sass/style.sass`](assets/sass/style.sass). If you make changes to the Sass while [running the site locally](#running), Hugo will automatically update the CSS and refresh the page in the browser.

## Contributing to this repo

This repository is managed by EasyCLA. Project participants must sign the free ([GraphQL Specification Membership agreement](https://preview-spec-membership.graphql.org) before making a contribution. You only need to do this one time, and it can be signed by [individual contributors](http://individual-spec-membership.graphql.org/) or their [employers](http://corporate-spec-membership.graphql.org/).

To initiate the signature process please open a PR against this repo. The EasyCLA bot will block the merge if we still need a membership agreement from you.

You can find [detailed information here](https://github.com/graphql/graphql-wg/tree/main/membership). If you have issues, please email [operations@graphql.org](mailto:operations@graphql.org).

If your company benefits from GraphQL and you would like to provide essential financial support for the systems and people that power our community, please also consider membership in the [GraphQL Foundation](https://foundation.graphql.org/join).