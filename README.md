# Templates

A collection of ready-to-adapt product templates for different kinds of businesses.
Each template ships as the set of products the business needs: for a shop or a cinema, a public website, an admin back office, a customer app and the backend API behind them; for a local-first tool, a single desktop app.

| Template | For | Products | Stack |
| --- | --- | --- | --- |
| [`cinema`](cinema) | Cinemas: listings, showtimes, seat booking, tickets | Backend, website, admin, customer app | Django, Astro, Angular, Flutter |
| [`wardrobe`](wardrobe) | Clothing stores: catalogue, sizes, stock, orders, returns | Backend, website, admin, customer app | Django, Astro, Angular, Flutter |
| [`finance`](finance) | Personal finance and investments, encrypted on the user's device | Desktop app | Python, pywebview, SvelteKit |
| [`wiki`](wiki) | A reference wiki built on a public API: every Pokémon, move, ability, type and game | Website, app | Astro, Flutter, PokéAPI |

Every brand, person and business in the demo data is fictional. The `wiki` template uses real game data from PokéAPI and is an unofficial fan reference.

## Requirements

Install only what the template you want to run needs:

| Tool | Version | Used by |
| --- | --- | --- |
| Git | any recent version | everything |
| Python | 3.12 or newer | `cinema` and `wardrobe` backends, `finance` |
| Node.js and npm | Node 22.22 or newer (or 24.15+) | websites, admins, the `finance` interface |
| Flutter | 3.44 or newer | `cinema` and `wardrobe` customer apps, the `wiki` app, plus Xcode (iOS) or Android Studio (Android) |

None of the templates needs a database server, a cloud account or a payment account to run locally. The `wiki` template needs an internet connection the first time it runs, to read PokéAPI.

## Getting started

Every template and every product is a Git submodule. Clone everything at once:

```bash
git clone --recurse-submodules https://github.com/mattoznav/templates.git
cd templates
```

If you already cloned without submodules:

```bash
git submodule update --init --recursive
```

Then open the README of the template you want to run: it walks through installing, configuring and starting each part, and how to sign in.

- [`cinema/README.md`](cinema/README.md): backend on port 8000, website on 4321, admin on 4200
- [`wardrobe/README.md`](wardrobe/README.md): backend on 8001, website on 4322, admin on 4201, so it can run next to the cinema
- [`finance/README.md`](finance/README.md): one desktop window
- [`wiki/README.md`](wiki/README.md): website on 4323, app on a simulator or device

Each product also has its own README with the details: data model, API, payment flow, structure and checks.

## Contributing

Read [`AGENTS.md`](AGENTS.md) before committing anything.
