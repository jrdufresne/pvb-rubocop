# pvb-rubocop

pvb-rubocop holds common configuration for [rubocop](https://github.com/rubocop/rubocop)
utility.

## Installation

```console
$ bundle add pvb-rubocop --group=development
$ bundle add rubocop --group=development
$ bundle add rubocop-performance --group=development
```

For Rails projects:

```console
$ bundle add rubocop-factory_bot --group=development
$ bundle add rubocop-rspec --group=development
```

## Usage

Add the following to the `rubocop.yml` file:

```yaml
inherit_gem:
  pvb-rubocop: default.yml
```

For Rails projects:

```yaml
inherit_gem:
  pvb-rubocop: rails.yml
```

For more details see rubocop documentation on
[inheriting configuration from a dependency gem](https://docs.rubocop.org/rubocop/configuration.html#inheriting-configuration-from-a-dependency-gem)

## Creating a release

1. Create a new pull request that:

- Bumps the version in `pvb-rubocop.gemspec`
- Updates `CHANGELOG.md` to include all noteworthy changes, the release
  version, and the release date.

2. After the pull request lands, checkout the most up to date `main` branch and
   build the gem:

```console
$ docker run --rm -it -v $(pwd):$(pwd) -w $(pwd) ruby gem build
```

3. Publish the gem:

```console
$ docker run --rm -it -v $(pwd):$(pwd) -w $(pwd) ruby gem push pvb-rubocop-X.Y.Z.gem
```

4. Create and publish a git tag:

```console
$ git tag X.Y.Z
$ git push https://github.com/Pioneer-Valley-Books/pvb-rubocop.git X.Y.Z
```
