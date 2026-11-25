# homebrew-tap

Homebrew tap of [cultoftheai](https://github.com/cultoftheai). This tap is shared with agent-id.

## Orbit

[Orbit](https://github.com/cultoftheai/orbit) runs coding agents in sandboxes on OrbStack.

Requirements: a Mac with Apple Silicon, Homebrew, and [OrbStack](https://orbstack.dev) (`brew install --cask orbstack`). Homebrew does not install OrbStack for you. Apple Silicon only: Intel Macs are not supported. Orbit is not affiliated with Anthropic; each user signs in to the agent with their own account.

The first Orbit release does not exist yet. Until it exists, `brew install` fails.

```sh
brew tap cultoftheai/tap
brew trust --formula cultoftheai/tap/orbit   # Homebrew 6+ asks to trust third-party code
brew install cultoftheai/tap/orbit
```

`brew install cultoftheai/tap/orbit` alone also works: a fully qualified name trusts only that item.

## Maintainers

The formula is built from the source tarball of a release tag. Updates arrive as PRs from the release workflow of Orbit that change `url` and `sha256` only; merge them (merge commit) once the CI is green. Nothing merges automatically.
