# Changelog

Unlike other Wall Brew repositories, `rebroadcast` does not use semantic versioning.
Since `rebroadcast` primarily supports automated actions and developer tooling, there is little to distinguish breaking changes and bug fixes.
That said, it is important to track the history of changes made to our CI/CD and documentation over time.

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

## 2023 Apr 18

* Bump `actions/checkout` to `3.5.2`

## 2023 Apr 01

* Bump `nnichols/clojure-dependency-update-action` to `v5`

## 2023 Mar 27

* Bump `actions/checkout` to `3.5.0`
* Bump `actions/checkout` to `3.3.0`

## 2022 Dec 13

* Add NPM files to .gitignore, since it's used for CLJS test suites
* auto-run sync on merge to master

## 2022 Dec 12

* Bump `actions/checkout` from `3.1.0` to `3.2.0`

## 2022 Dec 08

* Configure .gitignore as a rebroadcastable target
* Configure common Pull Request Label targets as rebroadcastable targets
* Add GitHub Action to check clojure documentation will produce valid cljdoc documentation
* Add GitHub Action to automatically generate the CONTRIBUTORS image
* Add GitHub action to greet new contributors
* Add template for Contribution Guidelines to embed repository-specific links
* Add template for MIT License to embed the repository year

## 2022 Dec 06

* Configure all common clojure Github Actions as rebroadcastable targets
* Configure static documentation templates as rebroadcastable targets
* Configure Pull Request and Issue Templates as rebroadcastable targets
* Configure clj-kondo and cljstyle configuration  as rebroadcastable targets
