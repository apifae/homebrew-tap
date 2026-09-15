# apifae/homebrew-tap

The Homebrew tap for APIFae, a command-line tool that mocks the HTTP APIs your
code depends on and tells you when those mocks stop matching the real API.

A mock is written once, but the API it stands in for keeps changing, and tests
that use the mock go on passing against responses the API no longer sends.
APIFae serves mocks from YAML files you commit, and `apifae diff` compares each
one with the live API. It exits 1 when a mock has drifted and 2 when it can't
reach the API, so a CI job can tell drift from an outage. `apifae patch` then
writes what it found back into your mocks.

APIFae is a single native binary with no runtime to install first. The CLI is
free and will stay free.

## Install

```sh
brew install apifae/tap/apifae
```

The `apifae/tap/` prefix is required. Installing the unprefixed name is not this
formula and will not work: that name belongs to homebrew-core, which APIFae is
not in.

The formula is generated on each release and installs a prebuilt binary; it does
not build from source. Upgrade with `brew upgrade apifae`.

## Learn more

[Getting started](https://apifae.com/docs/getting-started) takes an OpenAPI spec
to a served mock in about a minute. The guides and the command reference are at
<https://apifae.com>. Problems: <hello@apifae.com>.

## Licence

Closed source; binaries under MIT or Apache-2.0.
