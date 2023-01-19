# aspnet-react

Base template for most common DRS web apps

This repo is a work in progress while we put it together in a desirable form to allow quickly bootstrapping web apps.

Once it reaches a viable point for bootstrapping most new apps, it will morph into a living template that is regularly updated and augmented with new base features, and hopefully allow for easy downstream updates to apps previously created from the template.

# Template Wishlist

As we build up the template, we are striving to include the latest and best forms of things from our current suite of apps, to take forward into future apps with the least work.

There are also desirable improvements for future apps that aren't currently present in any of our apps.

## General

- [x] .editorconfig with team standards
- [ ] VS Code recommended extensions
- [ ] Sample dev docker-compose file for peripheral services (e.g. postgres)
- [ ] Version tracking feature changes to aid when to update existing apps?

## Javascript

- [ ] npm workspaces if possible; pnpm if not
- [ ] Vite for all JS app packages
- [ ] Storybook for JS (7+, native Vite)
- [ ] Typescript for all JS packages
- [ ] eslint typescript config
- [ ] eslint prettier exclusion
- [x] Prettier for all supported formats
- [x] Husky pre-commit hook for prettier
- [ ] core ui library package?
- [ ] Chakra theming of custom reusable components (e.g. ActionButton, SummaryCard) to allow easier per-project customisation without significant template deviation
- [ ] ASP.NET proxying for Vite SPA

## .NET

- [ ] Latest .NET (7 at time of writing)
  - keep the template on the latest (annual update)
  - keep apps on latest LTS (bi-annual update)
- [ ] Self serving built SPA
- [ ] MSBuild SPA inclusion config, custom publish config etc.
- [ ] Identity Server
- [ ] Configurable cookie vs OIDC auth?
- [ ] Clean "Startup" pattern
- [ ] CLI support in the aspnet app
- [ ] Razor Pages server auth (possibly with React or else Chakra CSS)

## Documentation

- [ ] Template documentation in this readme, or Github wiki if more space needed?
- [ ] Guidance for renaming the template apps for an actual project

  - [ ] js packages
  - [ ] dotnet sln, csproj, namespaces
  - the dotnet cli can do 90% of this if we use a custom template
    1. rename the `.sln` manually as desired
    1. `dotnet new <custom template path>`
    - this will allow setting the project name, which will handle namespaces and the csproj, cloning the template project to a new one.
    1. `dotnet sln add <new project>`
    1. `dotnet sln remove <custom template project>`
    1. Delete the template project folder
  - this will also allow in future the ability to parameterise aspects of the template **if desirable**
    - in practice we will probably _usually_ manage app feature inclusion based on runtime config rather than template config

- [ ] Docusaurus site in the template? (could contain common template docs too such as general use of Bicep, running db migrations...)

## CI/CD

- [ ] GitHub Actions for building all apps / libs on PRs
- [ ] GitHub Actions for publishing all outputs on merge to main
- [ ] GitHub Actions for enabling CD of apps to Azure?
- [ ] Azure Pipelines for building all apps / libs on PRs
- [ ] Azure Pipelines for publishing all outputs on merge to main
- [ ] Azure Pipelines for enabling CD of apps to Azure?
- [ ] General Bicep templates
- [ ] Guidance on customising deployment workflows
- [ ] Guidance on customising and running Bicep (including manual tasks)
