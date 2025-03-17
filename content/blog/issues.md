+++
title = "🚧 Issues"
+++


## Slides

- [ ] responsive design (for small display)
- [ ] Use tera variables c.f. `theme.toml`

- [x] スライドの区切りに `<section>` タグが必要
- [x] コードブロックがパースされない

  これらはおそらく markdown の contents を zola がどう parse するかの問題で、
  現状 `{{ page.content }}` で parse 済みの HTML が拾われるため。

  -> `highlight.js`, `markdown.js` を無効化してクリア

- [ ] `https://cdn.jsdelivr.net/npm/reveal.js` でいいのか
