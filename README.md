# Fable.MaterialUI.Icons

This package provides Fable bindings for Material-UI SVG icons. You can use it with [fable-material-ui](https://github.com/mvsmal/fable-material-ui) (>= 3.0.0 due to module/namespace clashes) or on its own.

## Installation

* Install the `@material-ui/icons` npm package and its peer dependency `@material-ui/core`:
  * using npm: `npm install @material-ui/icons @material-ui/core`
  * using yarn: `yarn add @material-ui/icons @material-ui/core`

* Install the bindings:
  * using dotnet: `dotnet add package Fable.MaterialUI.Icons`
  * using paket: `paket add Fable.MaterialUI.Icons`

## Usage

```f#
open Fable.Helpers.React
open Fable.MaterialUI.Icons

let view =
  div [ ] [
    homeIcon [ ]
  ]
```

For icon-specific properties, use [fable-material-ui](https://github.com/mvsmal/fable-material-ui) and see its [SvgIcon documentation](https://mvsmal.github.io/fable-material-ui/#/api/svg-icon).

## Missing new icons?

If the bindings are outdated, please file an issue and I'll update them. It's quick and simple (they're auto-generated), but I don't have the capacity for manually checking for changes in `@material-ui/icons`.

## Contributing/updating

1. Check the [Material-UI changelog](https://github.com/mui-org/material-ui/blob/master/CHANGELOG.md) for relevant changes
2. Run `yarn upgrade --latest`
3. Run `./fake.cmd build -t Update`
4. Check the HTML file in the `output` folder to verify that all icons render correctly
5. Update the version number in `src/Fable.MaterialUI.Icons/Fable.MaterialUI.Icons.fsproj`
6. Commit, tag (to trigger release from AppVeyor), and push
