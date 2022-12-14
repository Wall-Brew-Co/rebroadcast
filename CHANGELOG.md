# Changelog

Unlike other Wall Brew repositories, `rebroadcast` does not use semantic versioning.
Since `rebroadcast` primarily supports automated actions and developer tooling, there is little to distinguish breaking changes and bug fixes.
That said, it is important to track the history of changes made to our CI/CD and documentation over time.

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
* Add template for Contibution Guidelines to embed repository-specific links
* Add template for MIT License to embed the repository year

## 2022 Dec 06

* Configure all common clojure Github Actions as rebroadcastable targets
* Configure static documentation templates as rebroadcastable targets
* Configure Pull Request and Issue Templates as rebroadcastable targets
* Configure clj-kondo and cljstyle configuration  as rebroadcastable targets
