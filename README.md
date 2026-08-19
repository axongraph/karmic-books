# karmic-books — cover image hosting

Karmic Books' cover images, served publicly at **[https://images.krmc.shop](https://images.krmc.shop)** via GitHub Pages.

Referenced by the master catalog (`coverImageUrl`, `image_url_2..5`).
Managed by [`karmic covers`](https://github.com/axongraph/karmic) — see [AXO-167](https://linear.app/axongraph/issue/AXO-167).

## Layout

Files at repo root, keyed by ISBN and slot:

```
9780241609910/
  1.jpg     # primary — → master catalog coverImageUrl
  2.jpg     # → image_url_2
  3.jpg     # → image_url_3
  4.jpg     # → image_url_4
  5.jpg     # → image_url_5
```

URLs:

```
https://images.krmc.shop/9780241609910/1.jpg
https://images.krmc.shop/9780241609910/2.jpg
```

## Workflow

Do not push directly. Use the karmic CLI:

```
karmic covers upload --isbn 9780241609910 [--slot 1..5] path/to/cover.jpg
karmic covers list --isbn 9780241609910
```

Local staging clone lives at `~/.axon/data/karmic/images/`.
