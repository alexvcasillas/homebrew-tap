# alexvcasillas/tap

Homebrew formulae and casks for [alexvcasillas](https://github.com/alexvcasillas)'s tools.

Homebrew asks you to trust third-party taps before it installs from them. Trust this one
first:

```sh
brew trust alexvcasillas/tap
```

If `brew install` or `brew upgrade` says the tap is untrusted, run that command once.

## curl-runner

Run HTTP request suites defined in YAML, on libcurl. [Docs](https://www.curl-runner.com)

```sh
brew trust alexvcasillas/tap
brew install alexvcasillas/tap/curl-runner
```

Or tap once and use the short name:

```sh
brew tap alexvcasillas/tap
brew trust alexvcasillas/tap
brew install curl-runner
brew upgrade curl-runner
```

## curl-runner studio

The macOS app for curl-runner request files. macOS 12 or later, Apple silicon and Intel.

```sh
brew trust alexvcasillas/tap
brew install --cask alexvcasillas/tap/curl-runner-studio
```

The formula installs the prebuilt binaries from the
[curl-runner GitHub releases](https://github.com/alexvcasillas/curl-runner/releases)
(macOS and Linux, arm64 and x86_64), verified against each release's `SHA256SUMS.txt`.

## How updates work

`.github/workflows/update-curl-runner.yml` runs every hour. When curl-runner has a newer
release it regenerates `Formula/curl-runner.rb` with `scripts/update-curl-runner.sh`,
installs and tests it, then pushes. To update immediately, run the workflow by hand
(Actions → Update curl-runner → Run workflow).
