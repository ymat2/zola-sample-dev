+++
title = "🚧 Issues"
+++


## Slides

- [ ] スライドの区切りに `<section>` タグが必要
- [ ] コードブロックがパースされない

これらはおそらく markdown の contents を zola がどう parse するかの問題で、
現状 `{{ page.content }}` で parse 済みの HTML が拾われるため。

zola の高速? parse を生かしつつ、reveal.js の記法に従わせられればいいのだけど。。。
(shortcode?)

あるいはほとんどの機能を zola のやつを使うという手もある？
-> `highlight.js`, `markdown.js` を無効化してクリア

- [ ] `https://cdn.jsdelivr.net/npm/reveal.js` でいいのか
