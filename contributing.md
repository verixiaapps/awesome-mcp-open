# Contribution Guidelines

Thanks for helping keep **Awesome MCP Open** genuinely open. This isn't a
comprehensive index — it's a curated list of Model Context Protocol servers
you can run yourself. Please read this before opening a pull request.

## The bar for inclusion

Every entry must pass **all three** tests. If a server misses even one, it
doesn't belong here — no matter how good it is:

1. **Self-hostable** — you can run the server yourself, with no mandatory
   vendor endpoint in the loop.
2. **Open-source** — a real FOSS license, with source you can audit before
   granting it tool access.
3. **No lock-in** — it isn't dead without a paid proprietary backend, and it
   doesn't strand your data on someone else's servers.

Cloud-only servers and open clients that are useless without a paid API are
out of scope by design. That's not a knock on the tool — it's just not what
this list is for.

## Adding a server

- One server per pull request.
- Add it to the bottom of the most appropriate category.
- Format: `- **[Name](repo-url)** · Short, objective description of what it does`
- The description states what the server *does*, not that it's "awesome" or "the best."
- Start with a capital letter. Keep it to one line.
- Link to the **source repository**, not a marketing page.
- Add a red flag (`fiddly setup`, `heavy`, `unmaintained`) only when it
  genuinely applies and is verifiable on the repo page.

## Editing or removing

- Open a PR if a server has gone cloud-only, closed-source, unmaintained
  (archived or no commits in 6+ months), or otherwise stopped meeting the bar.
- Corrections to links, descriptions, or flags are always welcome.

## Quality checklist

- [ ] The server passes all three inclusion tests.
- [ ] The entry is in the right category, at the bottom.
- [ ] The description is objective, one line, and correctly capitalized.
- [ ] The link points to the source repository.
- [ ] Spelling and formatting match the surrounding entries.

By contributing, you agree to release your contributions under the CC0 license.
