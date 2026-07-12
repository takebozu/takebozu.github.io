# Lucid Works

Source for [lucidworks.app](https://www.lucidworks.app), the site for the iOS/macOS apps built by Lucid Works:

- [GridFinder for iOS](https://www.lucidworks.app/GridFinder/)
- [Lucid Reader for iOS](https://www.lucidworks.app/LucidReader/)
- [BoltClip for macOS](https://www.lucidworks.app/BoltClip/)

Built with Jekyll and hosted on GitHub Pages. The site content lives in `index.md` and each app's `index.md`; this README is not published to the site.

## Local development

```bash
bundle install        # first time only
bundle exec jekyll serve
```

Then open http://localhost:4000. The `Gemfile` pins the same `github-pages` gem GitHub uses in production, so the local preview matches what actually gets deployed. It is not used by the production build itself — GitHub Pages builds from the branch with its own pinned `github-pages` gem, ignoring the `Gemfile`.
