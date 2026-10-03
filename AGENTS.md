# Contributing rules

These rules apply to this repository and to every submodule inside it, for people and for AI agents alike.
Everything committed here is written as if the repository were already public.

## Language

- Everything is in English: code, identifiers, comments, commit messages, branch names, docs, UI copy, issues and pull requests.
- Sample content (movie titles, product names, addresses) is in English too, unless a template is explicitly about localisation.

## What never goes into git

- **Private notes and decisions.** Business plans, pricing, client conversations, personal opinions and "why I chose this" notes live in `.private/` (ignored by git) or outside the repository. Committed docs explain *how* the code works, not personal reasons behind it.
- **Real people and real businesses.** No real names, emails, phone numbers or addresses in code, seeds, fixtures, tests or screenshots. Use fictional brands and `example.com` addresses.
- **Client work.** Nothing copied from client projects: no names, logos, copy, data or domain-specific details that identify them.
- **Secrets.** No API keys, tokens, passwords, keystores, signing certificates or service account files. Commit a `.env.example` with placeholder values instead.
- **Infrastructure details.** No real hostnames, IP addresses, database URLs, cloud project or account IDs.
- **Assets without a clear license.** No real movie posters, trailers, brand logos, stock photos or fonts that cannot be redistributed. Use original, generated or openly licensed assets and note their source in the template's README.

## Writing style

- Comments explain intent, not history. No TODOs that reveal plans, deadlines or names; open an issue instead.
- Commit messages describe the change, not the context around it.
- Keep docs neutral: no first-person anecdotes or references to specific customers.

## Structure

- Each business vertical (for example `cinema`, `wardrobe`) is a submodule with its own repository.
- Inside each vertical, each product (`website`, `admin`, `customer-app`) is a submodule with its own repository.
- Repository names follow `templates-<vertical>` and `templates-<vertical>-<product>`.

## Before making a repository public

1. Search the full history, not just the latest commit, for secrets and personal data (for example with `gitleaks detect`).
2. Check that every submodule is public too, or the clone will fail for others.
3. Add a `LICENSE`.
4. Check commit author emails: use the GitHub `noreply` address.
