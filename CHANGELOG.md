# Changelog

Unlike other Wall Brew repositories, `rebroadcast` does not use semantic versioning.
Since `rebroadcast` primarily supports automated actions and developer tooling, there is little to distinguish breaking changes and bug fixes.
That said, it is important to track the history of changes made to our CI/CD and documentation over time.

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [2024 October 08](#2024-october-08)
- [2024 October 07](#2024-october-07)
- [2024 October 02](#2024-october-02)
- [2024 September 30](#2024-september-30)
- [2024 September 21](#2024-september-21)
- [2024 September 14](#2024-september-14)
- [2024 September 6](#2024-september-6)
- [2024 July 12](#2024-july-12)
- [2024 June 11](#2024-june-11)
- [2024 May 3](#2024-may-3)
- [2024 April 28](#2024-april-28)
- [2024 April 22](#2024-april-22)
- [2024 April 19](#2024-april-19)
- [2024 March 16](#2024-march-16)
- [2024 March 3](#2024-march-3)
- [2024 February 19](#2024-february-19)
- [2024 January 27](#2024-january-27)
- [2023 June 1](#2023-june-1)
- [2023 May 25](#2023-may-25)
- [2023 April 18](#2023-april-18)
- [2023 April 01](#2023-april-01)
- [2023 March 27](#2023-march-27)
- [2022 December 13](#2022-december-13)
- [2022 December 12](#2022-december-12)
- [2022 December 08](#2022-december-08)
- [2022 December 06](#2022-december-06)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## 2024 October 08

* Consistently format all GitHub Actions workflows
* Add an `id` to all steps in GitHub Actions workflows
* Add a `name` to all steps in GitHub Actions workflows
* Add inline comments to GitHub Actions
* Fix the formatting of the `cljstyle` config
* Suppress `clj-kondo` warnings for `clojure.core/*clojure-version*`

## 2024 October 07

* Update Renovate config to ignore GitHub Actions, since they are managed by this repository
* Update `actions/checkout` to `v4.2.1`

## 2024 October 02

* Update Renovate config to require NPM dependencies to have been available for a minimum of 3 days before updating
* Move renovate configuration to the `.github` directory

## 2024 September 30

* Configured several GitHub Actions to cancel previous runs when a new run is triggered
* Eliminated test runs against every push to a branch, only running tests on pull requests
* Label PRs with changes to bouncer files with 'restricted' and 'tooling'

## 2024 September 21

* Add [bouncer job](https://github.com/Wall-Brew-Co/bouncer) to the linting GitHub Action
* Jobs that require the Wall Brew PAT will now only run on non-forked copies of each repo

## 2024 September 14

* Update cljstyle rules for generative testing blocks
* Update clj-kondo to alert on implementation-only and experimental feature usage

## 2024 September 6

* Add [bouncer](https://github.com/Wall-Brew-Co/bouncer) to the list of supported repos

## 2024 July 12

* Automate the copying of CODEOWNERS configuration file

## 2024 June 11

* Update renovate to check all yaml files for GitHub Action updates, to automate dependency management of CI/CD

## 2024 May 3

* Use [sealog](https://github.com/Wall-Brew-Co/lein-sealog) to emit version information in `deploy_to_clojars.yml`
* Validate sealog state in `lint.yml`

## 2024 April 28

* Update `actions/checkout` to `v4.1.4`

## 2024 April 22

* Update `actions/checkout` to `v4.1.3`

## 2024 April 19

* Update `stefanzweifel/git-auto-commit-action` to `v5.0.1`

## 2024 March 16

* Update renovate to mark PRs as auto-mergable (requires review and passing tests)

## 2024 March 3

* Update `.cljstyle` config to ignore commonly uncommitted directories (e.g. `node_modules`, `target`)
* Update Misspell to ignore alternative spellings of "liter" and "milliliter"
* Update `sealog` config to pretty print changelog entry source files

## 2024 February 19

* Add default configuration for [Sealog](https://github.com/Wall-Brew-Co/lein-sealog)
* Update Renovate to progressively rebase branches
* Update Renovate to keep lockfiles up-to-date
* Update all comments to link to source file

## 2024 January 27

* Bump year to 2024
* Bump `actions/cache` to `v4`
* Bump `github/codeql-action/upload-sarif` to `v3`
* Bump `actions/labeler` to `v5`
* Bump `actions/checkout` to `4.1.1`
* Add new label types

## 2023 June 1

* Bump `actions/checkout` to `3.5.3`

## 2023 May 25

* Replace `clojure-dependency-update-action` with [Renovate](https://github.com/orgs/Wall-Brew-Co/discussions/5)
* Bump `clj-holmes-action` to 53daa4da4ff495cccf791e4ba4222a8317ddae9e
* Force Leiningen to keep POM files up-to-date

## 2023 April 18

* Bump `actions/checkout` to `3.5.2`

## 2023 April 01

* Bump `nnichols/clojure-dependency-update-action` to `v5`

## 2023 March 27

* Bump `actions/checkout` to `3.5.0`
* Bump `actions/checkout` to `3.3.0`

## 2022 December 13

* Add NPM files to .gitignore, since it's used for CLJS test suites
* auto-run sync on merge to master

## 2022 December 12

* Bump `actions/checkout` from `3.1.0` to `3.2.0`

## 2022 December 08

* Configure .gitignore as a rebroadcastable target
* Configure common Pull Request Label targets as rebroadcastable targets
* Add GitHub Action to check clojure documentation will produce valid cljdoc documentation
* Add GitHub Action to automatically generate the CONTRIBUTORS image
* Add GitHub action to greet new contributors
* Add template for Contribution Guidelines to embed repository-specific links
* Add template for MIT License to embed the repository year

## 2022 December 06

* Configure all common clojure Github Actions as rebroadcastable targets
* Configure static documentation templates as rebroadcastable targets
* Configure Pull Request and Issue Templates as rebroadcastable targets
* Configure clj-kondo and cljstyle configuration  as rebroadcastable targets
