# alexvcasillas/tap

Homebrew formulae for [alexvcasillas](https://github.com/alexvcasillas)'s tools.

## curl-runner

Run HTTP request suites defined in YAML, on libcurl. [Docs](https://www.curl-runner.com)

```sh
brew install alexvcasillas/tap/curl-runner
```

Or tap once and use the short name:

```sh
brew tap alexvcasillas/tap
brew install curl-runner
brew upgrade curl-runner
```

The formula installs the prebuilt binaries from the
[curl-runner GitHub releases](https://github.com/alexvcasillas/curl-runner/releases)
(macOS and Linux, arm64 and x86_64), verified against each release's `SHA256SUMS.txt`.

## How updates work

`.github/workflows/update-curl-runner.yml` runs every hour. When curl-runner has a newer
release it regenerates `Formula/curl-runner.rb` with `scripts/update-curl-runner.sh`,
installs and tests it, then pushes. To update immediately, run the workflow by hand
(Actions → Update curl-runner → Run workflow).
