## 3.0.0 (2026-01-28)

Split rubocop.yml into two files to support non-Rails projects:

- default.yml (cops that apply to all projects)
- rails.yml (cops that only apply to Rails projects)

## 2.4.0 (2025-08-18)

For the cop `Style/HashSyntax`, set the `EnforcedShorthandSyntax` option to `always`.

## 2.3.0 (2025-03-27)

Migrate rubocop-performance and rubocop-rspec to use RuboCop plugin feature.

## 2.2.0 (2025-03-04)

Migrate rubocop-performance and rubocop-rspec to use RuboCop plugin feature.

## 2.1.0 (2025-01-14)

Enable `Style/RequireOrder` cop.

## 2.0.0 (2024-10-10)

Remove Gem dependencies. Allow the consumers to decide on the version of the
dependencies to use.

## 1.0.0 (2024-10-09)

Initial release.
