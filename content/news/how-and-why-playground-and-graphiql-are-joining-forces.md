---
title: "Web Based GraphQL IDEs for the win: How & Why Playground & GraphiQL are joining forces"
type: announcements
layout: news-item
date: 2020-04-03
author: Rikki Schulte
summary: Playground and GraphiQL are joining forces to focus on a single codebase
event: SAN FRANCISCO
---

The initial first public commit to GraphiQL was in 2014.

When Lee, Hyo and Angel first published it, the intention was to create a minimal reference IDE development ecosystem for GraphQL. The goal was to give people the utility packages they needed to build their own web based or IDE tool, and a simple tool for folks to start learning and applying the language. At the time, LSP was not yet a commonly accepted standard, and VSCode had yet to become the near ubiquitous development tool it is today.

Fast forward to today, and GraphiQL is now used by GraphQL implementations in dozens of languages, frameworks and runtimes.  It's used for everything from HTTP operations, to querying local schemas and even for developing IOT platforms.

### **Enter Playground**

Alongside GraphiQL, many of us are familiar with it's sibling- the handsome & feature-full [GraphQL Playground](https://github.com/prisma-labs/graphql-playground). Following GraphiQL's lead, it uses our `codemirror-graphql` (Insomnia, Alatair and others are also in this club!). This is why there are so many similarities between the direct editing experience of these tools.

Playground is *exactly* what we wanted to happen. It helped drive the development of our language ecosystem, and gave users an easier option than the more customization-oriented GraphiQL.  It provided a ton of excellent features - `graphql-config` support, multiple tabs, i18n, and http server middlewares.

### **Prisma Donates Playground to GraphQL Foundation**

As many have successfully guessed, **Prisma *is* donating Playground to the GraphQL Foundation.** Entering 2019 Prisma envisioned an eventual Playground 2.0 but then the advent of a modular GraphiQL 2 project showed an opportunity for great synergy, made all the more natural by Prisma's pivot toward modular database tooling for developers.

Playground 1.x has been a community effort of [dozens of contributors](https://github.com/prisma-labs/graphql-playground/graphs/contributors). Prisma thanks all contributors who helped out along the way. Prisma remains deeply committed to supporting the future of the GraphQL language. For example the [Prisma Labs team](https://github.com/prisma-labs) continues to focus on GraphQL API layer and [recently announced](https://github.com/prisma-labs/nexus/issues/373) the transition of [Nexus](https://nexus.js.org/) from a schema building library into a full [fledged GraphQL API framework](https://www.nexusjs.org).

### The Playground Features you love

In the interest of parity, we will keep a lot of the same features, whether by introducing them to the core or proving plugins that will ship with the playground preset.

- multiple tabs (GraphiQL Core)
- headers tab per operation tab (plugin)
- tracing tab (plugin)
- playground doc explorer (plugin)
- internationalization (GraphiQL Core)
- `graphql-config` support
- easy to use middlewares

### New Features

These new features will come with the new GraphiQL stable, for free!

- vscode style command palette (via `monaco-editor`)
- jump to fragment or other type definitions
- generate a collection of operations from your project's source files
- more customizeable network options - default headers per project, as well as headers per-operation
- helpers for integrating custom authentication flows
- extensive theme, layout, and component customization abilities (you can start with the playground theme preset and work from there!)
- custom tabs and panels

### How will it be re-implemented?

Playground 2.0 will be a GraphiQL preset that includes the custom theme as well as the custom playground doc explorer plugin (as an alternative to the new doc explorer proposed by @orta and other users), HTTP headers and tracing tab plugins. You can find more technical detail, ongoing discussion and things to work on the [GraphiQL Plugin API Meta Issue](https://github.com/graphql/graphiql/issues/983) or in [other playground related discussion issues](https://github.com/graphql/graphiql/issues?q=label%3Agraphql-playground-preset) in the GraphiQL monorepo. 

While the Playground team's baseline goal will be relative parity with Playground 1.0, the team will be accepting proposals for new features and plugins that build on the existing GraphQL Playground experience. The [Features Roundup](https://github.com/graphql/graphiql/projects/10) project is a great place to see what we have planned already for plugins that Playground's preset can use, or you can also create a proposal if you don't see what you're looking for.

## `graphql-playground` repository next steps

The existing grpahql-playground will get one or two more maintenance/bugfix releases before being archived. You can still fork it of course. You can learn more about this in [the graphql-playground issue](https://github.com/prisma-labs/graphql-playground/issues/1143) we created for this migration.

### Call for Contributors

We're also looking for contributors to form a team to develop, support and maintain a playground preset. The goal would be for them to help iterate on and stabilize the plugin API effort, as well as work towards the effort of contributing to and maintaining the playground preset and it's associated plugins. If you are interested leave comment in the [Call for Contributors Gitub issue](https://github.com/graphql/graphiql/issues/1443).

You can also follow the [Plugin API Proposal discussion issue](https://github.com/graphql/graphiql/issues/983) for updates.
