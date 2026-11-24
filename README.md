# qizhanchan/homebrew-tap

Homebrew tap for qizhanchan's apps.

## go-code

A code editor for Go and other languages (macOS 13+, Apple Silicon).

```bash
brew install --cask qizhanchan/tap/go-code
```

Naming the cask in full (`qizhanchan/tap/go-code`) also trusts it under
Homebrew 7's [tap trust](https://docs.brew.sh/Tap-Trust); otherwise run
`brew trust --cask qizhanchan/tap/go-code` first.

Upgrade with `brew upgrade --cask go-code`, remove with `brew uninstall --cask go-code`
(`--zap` also removes settings, caches and logs).

go-code is not signed with an Apple Developer ID. The cask signs nothing itself;
it clears the quarantine flag on the installed app so macOS lets it start.
If you install the DMG from the releases page by hand instead, right-click the
app › Open the first time, or run
`xattr -dr com.apple.quarantine /Applications/go-code.app`.

## Maintaining

`Casks/go-code.rb` and the release assets are produced by q-code-editor's
`cmd/go-code/packaging/macos/app.sh release` (DMG → GitHub release here →
cask commit). Do not edit the cask by hand.
