# Villain Layer for Homebrew

[Villain Layer](https://github.com/Villain-Studios/villain-layer) runs
coding-agent CLIs in terminals, one git worktree per ticket. For macOS 27.

```bash
brew tap villain-studios/tap
brew trust --cask villain-studios/tap/villain-layer
brew install --cask villain-layer
```

`brew upgrade` updates it. Quit Villain Layer first, and run it from a
terminal outside the app: replacing the app while it runs kills it, and
every agent running in it, so the cask refuses to.

`brew trust` is needed because Homebrew runs nothing from a tap it has not
been told to trust. Without it, `brew upgrade` does not load the cask.

## Changing the cask

Not here. `Casks/villain-layer.rb` is written by the app's release workflow
from [`packaging/homebrew/villain-layer.rb`](https://github.com/Villain-Studios/villain-layer/blob/main/packaging/homebrew/villain-layer.rb)
each time a release is published, and anything changed here is overwritten.
