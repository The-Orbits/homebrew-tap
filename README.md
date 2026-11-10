# The-Orbits/homebrew-tap

Homebrew formulae and casks for [Orbits](https://orbits.africa).

```sh
brew install The-Orbits/tap/orbits
```

installs the [Orbits CLI](https://docs.orbits.africa/cli), with shell completion for bash, zsh and fish. Upgrade it
with `brew upgrade orbits`.

## How it is updated

Nothing here is edited by hand. Each release of [The-Orbits/orbits-cli](https://github.com/The-Orbits/orbits-cli)
(a pushed tag) runs GoReleaser, which rewrites `Casks/orbits.rb` with the new version, its download URLs and their
sha256 sums, and commits it here as `orbits vX.Y.Z`. A pre-release (`v0.2.0-rc.1`) leaves the cask where it was.

The release authenticates with `HOMEBREW_TAP_TOKEN`, a token in orbits-cli's secrets that may write to this repository
and nothing else.

The CLI runs on macOS and Linux (Homebrew on Linux too), on arm64 and amd64. Its binary is not notarized, so the cask
clears macOS's quarantine flag on install.
