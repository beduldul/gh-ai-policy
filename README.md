# gh-ai-policy

A [gh](https://cli.github.com) extension for
[ai-policy](https://github.com/beduldul/ai-policy): check whether a repository
accepts AI-assisted contributions before you open the pull request.

## Install

```sh
gh extension install beduldul/gh-ai-policy
```

## Usage

```sh
gh ai-policy pallets/click
gh ai-policy --explain stablyai/orca
gh ai-policy --path .
gh ai-policy --json go-playground/validator
```

Everything after `gh ai-policy` is passed straight to the `ai-policy` binary,
so the flags and exit codes are the same. See the
[main README](https://github.com/beduldul/ai-policy#readme).

## How it works

The script downloads the release binary for your platform on first run and
caches it under `${XDG_CACHE_HOME:-~/.cache}/gh-ai-policy/<tag>/`. To pull a
newer release, set `GH_AI_POLICY_REFRESH=1`.

Supported: macOS and Linux, `arm64` and `amd64`.

## License

MIT
