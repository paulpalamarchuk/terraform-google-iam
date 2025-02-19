# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog][keep-a-changelog],
and this project adheres to [Semantic Versioning][semantic-versioning].

Extending the adopted spec, each change should have a link to its
corresponding pull request appended.

## [Unreleased]

## [2.1.0] - 2019-YY-ZZ

### Added

- Submodules for each type of binding. [#43]

### Fixed

- Fix issue with long IAM bindings list. [#32]
- Allow referencing computed values. [#43]

## [2.0.0] - 2019-07-16

### Changed

- Supported version of Terraform is 0.12. [#24] [#29]

## [1.1.1] - 2019-05-29

### Fixed

- Updated folders input to accept either `folders/<id>` or `<id>`. [#19]

## [1.1.0] - 2019-05-03

### Added

- Clarification of [additive and authoritative modes in README][modes].
  [#5]
- A [Stackdriver Agent Roles example][stackdriver-agent-roles-example].
  [#12]

### Changed

- The [subnet example][subnet-example] constructs the required fully
  qualified subnet IDs using a `project` variable, a `region` variable,
  and the `subnet_one` and `subnet_two` variables. [#6] [#14]
- The [usage example in the README][usage-example] demonstrates a
  Terraform Module registry reference. [#7]
- The examples pin the `google` and `google-beta` providers to
  `~> 1.20`. [#9]

## [1.0.0] - 2018-09-26

This is the initial release of the module, with support for bulk IAM
management.

[modes]: README.md#additive-and-authoritative-modes
[keep-a-changelog]: https://keepachangelog.com/en/1.0.0/
[semantic-versioning]: https://semver.org/spec/v2.0.0.html
[stackdriver-agent-roles-example]: examples/stackdriver_agent_roles
[subnet-example]: examples/subnet
[usage-example]: README.md#usage

[Unreleased]: https://github.com/terraform-google-modules/terraform-google-iam/compare/v2.0.0...HEAD
[2.0.0]: https://github.com/terraform-google-modules/terraform-google-iam/compare/v1.1.1...v2.0.0
[1.1.1]: https://github.com/terraform-google-modules/terraform-google-iam/compare/v1.1.0...v1.1.1
[1.1.0]: https://github.com/terraform-google-modules/terraform-google-iam/compare/v1.0.0...v1.1.0
[1.0.0]: https://github.com/terraform-google-modules/terraform-google-iam/releases/tag/v1.0.0

[#5]: https://github.com/terraform-google-modules/terraform-google-iam/pull/5
[#6]: https://github.com/terraform-google-modules/terraform-google-iam/pull/6
[#7]: https://github.com/terraform-google-modules/terraform-google-iam/pull/7
[#9]: https://github.com/terraform-google-modules/terraform-google-iam/pull/9
[#12]: https://github.com/terraform-google-modules/terraform-google-iam/pull/12
[#14]: https://github.com/terraform-google-modules/terraform-google-iam/pull/14
[#19]: https://github.com/terraform-google-modules/terraform-google-iam/pull/19
[#24]: https://github.com/terraform-google-modules/terraform-google-iam/pull/24
[#29]: https://github.com/terraform-google-modules/terraform-google-iam/pull/29
[#32]: https://github.com/terraform-google-modules/terraform-google-iam/pull/32
[#43]: https://github.com/terraform-google-modules/terraform-google-iam/pull/43
