# rebroadcast

A repository for files that are copied across multiple repositories.

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [Rationale](#rationale)
- [Supported Files](#supported-files)
  - [Clojure](#clojure)
    - [cljstyle Configuration](#cljstyle-configuration)
    - [clj-kondo Configuration](#clj-kondo-configuration)
  - [Community Documentation](#community-documentation)
    - [Code of Conduct](#code-of-conduct)
    - [Security Policy](#security-policy)
    - [License](#license)
    - [Code Owners](#code-owners)
    - [Contribution Guidelines](#contribution-guidelines)
  - [GitHub Dot Files](#github-dot-files)
    - [Git Ignore Configuration](#git-ignore-configuration)
    - [Issue Templates](#issue-templates)
      - [Bug Report](#bug-report)
      - [Feature Request](#feature-request)
    - [GitHub Action Workflows](#github-action-workflows)
    - [Repository Labels](#repository-labels)
    - [Pull Request Template](#pull-request-template)
- [Unsupported Files](#unsupported-files)
- [Developing](#developing)
  - [Adding New Files](#adding-new-files)
  - [Targeting New Repositories](#targeting-new-repositories)
- [Rebroadcast License](#rebroadcast-license)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Rationale

The [Wall Brew Open Source Guidelines](https://github.com/Wall-Brew-Co/open-source) encourage a seamless and consistent developer experience.
While we often think about the work required to provide the tools, documentation, and automation behind that experience; we would do ourselves a disservice to ignore the cost of maintaining these files across a growing number of repositories.
To prevent individual repositories from falling out of sync, `rebroadcast` was established to be the primary source of truth for these files.

- [Template Community Documents](https://github.com/Wall-Brew-Co/open-source#template-community-documents)
- [Automating Opinions](https://github.com/Wall-Brew-Co/open-source#automating-opinions)

## Supported Files

### Clojure

Since most Wall Brew repositories are written in Clojure/Clojurescript, there are several language-specific configuration files worth sharing across repositories.
These configuration files work with the tools in the GitHub actions for those repositories, as well as the Leiningen plugins available during development.

#### cljstyle Configuration

[cljstyle](https://github.com/greglook/cljstyle) is used to automatically format all clojure(script) code at Wall Brew.
Further, each application uses the same cljstyle configuration to maintain as consistent of a look and feel as possible.
While the [configuration](./sources/clojure/.cljstyle) is minimal, rebroadcasting the file minimizes the cost of any future extension or change.

#### clj-kondo Configuration

[clj-kondo](https://github.com/clj-kondo/clj-kondo) is used as the primary linting too for clojure(script) code at Wall Brew.
Aside from a few special rules and hooks, most applications and all libraries, are generally able to leverage the same [linter configuration](./sources/clojure/config.edn).
The configuration is designed to cleanly integrate with code quality tools, and to push developers towards consistent coding standards.

### Community Documentation

Several community documents establish policies for all Wall Brew repositories.
Since Github leverages these files on a per-repository basis to display contextual links and information; therefore, a full-text copy must exist locally.

#### Code of Conduct

All community members should have a clear and shared understanding of what is considered acceptable and unacceptable behavior.
To prevent ad-hoc or just-in-time rule setting, we have explicitly outlined our expectations and rules in text.
The Code of Conduct strives to meet three goals:

- Welcome contributors and participants
- Define basic standards and rules for community participation
- Outline procedures for handling abuse and violation of said rules and standards

[This document is automatically linked for external contributors opening issues and pull requests if it is named `CODE_OF_CONDUCT.md`](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/adding-a-code-of-conduct-to-your-project)

#### Security Policy

Wall Brew maintains one standard policy for communicating repository and dependency vulnerabilities.
To streamline communication od sensitive and time-critical information, this files should be made uniformly available as `SECURITY.md`.
This also automatically populates the [Security Advisory](https://docs.github.com/en/code-security/getting-started/adding-a-security-policy-to-your-repository) tab in Github.

#### License

Barring exception, [all Wall Brew libraries are provided under the MIT License.](https://github.com/Wall-Brew-Co/open-source#licensing)
Common convention, and the literal text of the MIT license, require that it is provided alongside any repository or piece of software covered by that license.
Since it must contain the exact text of the license, we rebroadcast it undecorated without metadata/comments about this repository.

#### Code Owners

GitHub repositories allow owners to automatically assign Pull Request reviewers based off of impacted files in a [CODEOWNERS file.](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners)
Publicly available libraries are owned collectively by all members of the Wall Brew organization, and a basic configuration notifies us of Pull Requests more efficiently.

#### Contribution Guidelines

[Contributor guidelines](https://github.com/Wall-Brew-Co/open-source#contributor-guidelines) set explicit, upfront expectations around contributions to our open source repositories.
This includes additional information about of the actions/requests that Wall Brew maintainers and automated entities may take, outline that all contributions must adhere to any applicable intellectual property laws, and outlines that all contributions must be made in good-faith adherence to the Code of Conduct.

### GitHub Dot Files

Since most Wall Brew repositories are written in Clojure/Clojurescript, and we encourage tools to work out of the box with no to minimal configuration, our automated quality checks and tests can be shared across repositories.
Additionally, these files allow us to specify common bug report, feature request, and pull request templates.
These provide a uniform experience for developers across all of our repositories.

#### Git Ignore Configuration

[gitignore](https://git-scm.com/docs/gitignore) is used to automatically prevent the inclusion of unwanted files in Git.
Projects often maintain these files to ignore binary artifacts, build tool logs, temporary files generated by the project and its core tools.
Additionally, common development tools or operating system level files may be included too.
Files generated during individual development generally should not be added to project gitignore files, and should be ignored at the [user level.](https://gist.github.com/subfuzion/db7f57fff2fb6998a16c)

#### Issue Templates

Issue Templates prompt users for some basic information while raising GitHub issues.
Since most of Wall Brew's public repositories are Clojure libraries, we often need the same information to diagnose issues and field requests.
These markdown templates auto-format user provided reports, and streamline providing information to us.

##### Bug Report

While diagnosing issues or problems, we often need additional context or information to identify the root cause.
This includes but is not limited to the consumer's Clojure version, the deployment/development environment, and the usage context.
A template provides a proactive context in which this information may be provided.

##### Feature Request

Wall Brew's offerings are most commonly informed by our own development processed and needs; however, our end user may also identify their own needs.
To request these additions to our offerings, we usually need additional information to understand their needs and desires.
A template provides a proactive context in which this information may be provided.

#### GitHub Action Workflows

To provide a consistent experience to developers contributing to Wall Brew repositories, we apply consistent CI/CD actions to as many repositories as possible.
These include quality controls, like testing and linting, as well as development convenience tools, like automatic labelers and deployment tooling.
Historically, these were manually synchronized between repositories.

#### Repository Labels

Several of our GitHub actions automatically tag Pull Requests with labels useful for filtering lists.
Creating these idempotently within actions causes the description and color setting sto be lost.
While losing the label color is annoying, the description is used to render alt text for the badges displayed to represent each label.
Therefore, it's critical to maintain the description for users that rely on alt text.

#### Pull Request Template

New contributors often need guidance or reminders on the manual steps in our change process.
Additionally, we can prompt contributors to provide some high level information about their changes.
For that reason, we use a standard Pull Request Template in each of our repositories.

## Unsupported Files

It is just as important to denote which files are poor candidates for inclusion in `rebroadcast`

- GitHub Actions and development tools unique to individual repositories, such as the deployment tooling for the Brew Bot UI
- Files which are automatically generated as the result of development tools

## Developing

This repo is not intended for outside revision; however, it is critical to note how we can update and support our internal offerings as well.

### Adding New Files

New files that will be replicated to several projects should be added within the `sources` folder.
That folder is segmented into several high-level groups, and new files should be added to their most relevant section.
For example, the `community` subfolder for documentation like our Security policy.
After adding the file, add a description of its value to the README.
Finally, add it to each repository in the [sync configuration.](.github/sync.yml)
Information on that file's configuration may be found in the [repo-file-sync-action](https://github.com/BetaHuhn/repo-file-sync-action) repository.

### Targeting New Repositories

WallBrewBot should automatically posses the correct access to each repository within the Wall Brew GitHub organization.
To add a new repository, add it to the [sync configuration](.github/sync.yml) and any files you wish to be synchronized to that repository.
Information on that file's configuration may be found in the [repo-file-sync-action](https://github.com/BetaHuhn/repo-file-sync-action) repository.

## Rebroadcast License

Copyright © 2022 - [Wall Brew Co](https://wallbrew.com/)

This software is provided for free, public use as outlined in the [MIT License](https://github.com/Wall-Brew-Co/rebroadcast/blob/master/LICENSE)
