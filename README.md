# (Proposal) Standard Code Style Configurations Across The Company

## Current Situation

Currently, each team and project within the company has its own unique code style. This can create inconsistencies in the codebase and make it challenging for developers to understand and maintain each other's code.

## Change Vision

To solve this issue, it is important to establish standardized code style configurations across the company. By doing so, developers can easily read and work on any codebase within the organization, regardless of the team or project they are working on. Additionally, it will ensure a consistent pipeline stage for checking the code quality.

## Proposed Solutions

The goal is to have a minimal eslintrc configuration that should be used for each technology/stack in the company.

For each project, use the respective eslintrc and prettierrc config files as the base configurations. You can extend the eslint plugins by adding more plugins based on your use case, but you cannot remove any from the main configurations.

For each project, the main prettierrc configurations should not be edited or have additional rules added to them.

If we agree that a certain eslint plugin is necessary for all teams, we include it in the main configurations file.

## Contribution

If anyone has a suggestion or addition to update the current configuration, they can create a new pull request to apply the change. The pull request should be accepted by ALL team leads before it is merged and becomes part of our standard

## Prettier

We execute Prettier through ESLint by enforcing its rules, so there is no need to run a separate Prettier check. However, should we get rid of Prettier compatibility? Although ESLint can handle both code quality and formatting rules, configuring formatting solely through ESLint is generally more verbose. Plus, you may miss out on some of Prettier's opinionated but consistent formatting

## Stacks

* [NodeJs - TypeScript](/typescript/node)
* [NuxtJs - TypeScript](/typescript/nuxt)
* [NodeJs - JavaScript](/javascript/node)
* [NuxtJs - JavaScript](/javascript/nuxt)
