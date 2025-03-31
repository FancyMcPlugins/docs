# Development Guidelines

> The documentation has been moved to [https://docs.fancyplugins.de/](https://docs.fancyplugins.de/)
> This documentation might be outdated and will not be updated anymore.
{style="warning"}

This topic is all about the development guidelines that we follow at FancyPlugins. It is important to follow these
guidelines to maintain the quality of the code and to make sure that the code is consistent and easy to read.

## Pull Requests

Generally pull requests are welcome. However, it is important to follow the guidelines below when creating a pull
request.

If you plan to make a major change to the code, please join our discord server and discuss it with us before creating a
pull request out of nowhere.

### Code Style

Please try to adapt to the code style that is already present in the project. If you are unsure about the code style,
please join our discord server and ask for help.

If you have suggestions for a better code style, please join our discord server and discuss it with us.

### Commit Messages

Please make sure that your commit messages are clear and concise. It is important to write a good commit message so that
it is easy to understand what the commit is about.

Keep the commit message short and to the point. If you need to write a longer message, please use the body of the
commit.

### Testing

Please make sure that your code is tested before marking the pull request as ready for review. This means that the code
should compile and run without any errors. If you are unsure about how to test your code, please join our discord server
and ask for help.

When creating a PR for FancyNpcs please run the `/fancynpcs test` command in-game and attach a screenshot of the output
to the PR.

### Documentation

Please add documentation to your code. This means that you should add comments to your code so that it is easy
to understand what the code is doing. Also, please add Javadocs to the code if it is a public API.

If you modified, added or removed any commands, please update the `/npcs help` messages and the docs in the [docs
reposiotry](https://github.com/FancyMcPlugins/docs).

## Versioning

The version is structured as follows: `major.minor.patch.<build id>`. The build id is optional and is only used for
development builds.

### Major

The major version is increased when there are very significant changes to the codebase. This could be a complete rewrite
of the codebase or a major change in the way the plugin works. This is usually not done very often. When the major
version is increased, the minor and patch versions are reset to 0.

Data might be lost when updating to a new major version.

Breaking changes in the API are expected when updating to a new major version.

### Minor

The minor version is increased when there are new features added to the codebase. This could be new commands, new
features or support for a new minecraft version. This is done more often than increasing the major version. When the
minor version is increased, the patch version is reset to 0.

Data will not be lost when updating to a new minor version.

Breaking changes in the API are expected when updating to a new minor version.

### Patch

The patch version is increased when there are bug fixes or small changes to the codebase. This is done very often.

Data will not be lost when updating to a new patch version.

Breaking changes in the API are not expected when updating to a new patch version.

### Build

The build id is optional and is only used for development builds. The build id is increased every time a new build is
created.

Development builds are not recommended for production use.

Development builds might contain bugs.

Development builds might contain incomplete features.

Development builds might contain breaking changes.

Development builds might contain experimental features.

Development builds might contain untested features.

Development builds might contain unoptimized code.

Development builds might contain security vulnerabilities.

Development builds might contain incomplete documentation.

Development builds might cause data loss.

Development builds might cause server crashes.

Development builds might cause server lag.

Development builds might cause other issues.

## Changelog

Every release should have a changelog. The changelog will be added to all platforms where the plugin is available. The
changelog should contain the following information:

- The version number
- A list of changes that were made in this release
- A list of bug fixes that were made in this release
- A list of new features that were added in this release

There are mostly changes list that are important to server admins. Breaking changes to the API might not be listed in
the changelog.