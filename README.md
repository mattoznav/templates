# Templates

A collection of ready-to-adapt product templates for different kinds of businesses.
Each template ships as the set of products the business needs: for a shop or a cinema, a public website, an admin back office, a customer app and the backend API behind them; for a local-first tool, a single desktop app.

| Template | For | Products | Stack |
| --- | --- | --- | --- |
| [`cinema`](cinema) | Cinemas: listings, showtimes, seat booking, tickets | Backend, website, admin, customer app | Django, Astro, Angular, Flutter |
| [`wardrobe`](wardrobe) | Clothing stores: catalogue, sizes, stock, orders, returns | Backend, website, admin, customer app | Django, Astro, Angular, Flutter |
| [`finance`](finance) | Personal finance and investments, encrypted on the user's device | Desktop app | Python, pywebview, SvelteKit |
| [`wiki`](wiki) | A reference wiki built on a public API: every Pokémon, move, ability, type and game | Website, app | Astro, Flutter, PokéAPI |
| [`bnb`](bnb) | Bed & breakfasts: a 3D tour of the house, room by room, with booking links | Website | Astro, React Three Fiber, GSAP, Blender |

Every brand, person and business in the demo data is fictional. The `wiki` template uses real game data from PokéAPI and is an unofficial fan reference. The `bnb` model is dressed with CC0 assets from Poly Haven.

## Live demos

The public websites are published with GitHub Pages from their own repositories. The cinema and the shop run as static showcases, without their backend: accounts, bookings and orders are kept in the visitor's browser and no payment is taken.

- Cinema: [mattoznav.github.io/templates-cinema-website](https://mattoznav.github.io/templates-cinema-website/)
- Clothing store: [mattoznav.github.io/templates-wardrobe-website](https://mattoznav.github.io/templates-wardrobe-website/)
- Wiki: [mattoznav.github.io/templates-wiki-website](https://mattoznav.github.io/templates-wiki-website/)
- B&B: [mattoznav.github.io/templates-bnb-website](https://mattoznav.github.io/templates-bnb-website/)

## Requirements

Install only what the template you want to run needs:

| Tool | Version | Used by |
| --- | --- | --- |
| Git | any recent version | everything |
| Python | 3.12 or newer | `cinema` and `wardrobe` backends, `finance` |
| Node.js and npm | Node 22.22 or newer (or 24.15+) | websites, admins, the `finance` interface |
| Flutter | 3.44 or newer | `cinema` and `wardrobe` customer apps, the `wiki` app, plus Xcode (iOS) or Android Studio (Android) |
| Blender | 5.2 or newer | only to rebuild the `bnb` 3D model; the built model is included |

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
- [`bnb/README.md`](bnb/README.md): website on 4324

Each product also has its own README with the details: data model, API, payment flow, structure and checks.

## Contributing

Read [`AGENTS.md`](AGENTS.md) before committing anything.

## License

The code is released under the [MIT License](LICENSE). Each template keeps the licenses of its own third-party data, listed in its README.
