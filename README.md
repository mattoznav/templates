# Templates

A collection of ready-to-adapt product templates for different kinds of businesses.
Each template ships as the set of products the business needs: for a shop or a cinema, a public website, an admin back office, a customer app and the backend API behind them; for a local-first tool, a single desktop app.

| Template | For |
| --- | --- |
| [`cinema`](cinema) | Cinemas: listings, showtimes, tickets |
| [`wardrobe`](wardrobe) | Clothing stores: catalogue, sizes, orders |
| [`finance`](finance) | Personal finance and investments, encrypted on the user's device |

## Getting started

Every template and every product is a Git submodule. Clone everything at once with:

```bash
git clone --recurse-submodules https://github.com/mattoznav/templates.git
```

If you already cloned without submodules:

```bash
git submodule update --init --recursive
```

## Contributing

Read [`AGENTS.md`](AGENTS.md) before committing anything.
