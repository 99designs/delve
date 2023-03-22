![Delve](https://raw.githubusercontent.com/go-delve/delve/master/assets/delve_horizontal.png)

[![license](http://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/go-delve/delve/master/LICENSE)
[![GoDoc](https://godoc.org/github.com/go-delve/delve?status.svg)](https://godoc.org/github.com/go-delve/delve)
[![Build Status](https://delve.teamcity.com/app/rest/builds/buildType:(id:Delve_AggregatorBuild)/statusIcon.svg)](https://delve.teamcity.com/viewType.html?buildTypeId=Delve_AggregatorBuild&guest=1)

The GitHub issue tracker is for **bugs** only. Please use the [developer mailing list](https://groups.google.com/forum/#!forum/delve-dev) for any feature proposals and discussions.

### About Delve

- [Installation](Documentation/installation)
- [Getting Started](Documentation/cli/getting_started.md)
- [Documentation](Documentation)
  - [Command line options](Documentation/usage/dlv.md)
  - [Command line client](Documentation/cli/README.md)
  - [Plugins and GUIs](Documentation/EditorIntegration.md)
  - [Frequently Asked Questions](Documentation/faq.md)
- [Contributing](CONTRIBUTING.md)
  - [Internal Documentation](Documentation/internal)
  - [API documentation](Documentation/api)
  - [How to write a Delve client](Documentation/api/ClientHowto.md)

Delve is a debugger for the Go programming language. The goal of the project is to provide a simple, full featured debugging tool for Go. Delve should be easy to invoke and easy to use. Chances are if you're using a debugger, things aren't going your way. With that in mind, Delve should stay out of your way as much as possible.

## Releases

This uses (GoReleaser](https://goreleaser.com) to build and release go binaries. There is a GitHub Actions workflow configured to run this on any new tags pushed. In order to create a new release, from the master branch:

```
git tag vx.x.x e.g. v1.0.0
git push --tags
```

This should trigger the workflow to automatically create a new release. Once it has run, you should see a new release at https://github.com/99designs/ior/releases. Currently GoReleaser is configured to autogenerate a changelog based on commits.

The configuration for GoReleaser is in [.goreleaser.yaml](./.goreleaser.yaml). This specifies what operating systems and architectures to build for along with any other customization we want. You can read more about what can be configured here: https://goreleaser.com/customization/
