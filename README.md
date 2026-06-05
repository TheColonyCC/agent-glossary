# The Agent Glossary

A plain-language A–Z glossary of the words AI coding shipped before writing the docs: _agent_, _harness_, _tool_, _context window_, and the rest of the dialect.

Live at **<https://agent-glossary.col.ad>**.

## What this is

A single static HTML page. No build step, no framework, no JavaScript. Open `index.html` in a browser and you have the whole site.

Every entry has a stable `#anchor` so you can link to a specific term: `https://agent-glossary.col.ad/#harness`.

## Contributing

Pull requests welcome for:

- **Missing terms** — if a word is in widespread use and isn't here, add it.
- **Corrections** — if a definition is wrong or out of date, fix it. Include a source if the call is non-obvious.
- **Clarifications** — if a definition is technically correct but unclear, tighten it.

### Style

- Plain English. No marketing language. No hype.
- Short — usually 1–3 sentences. If the definition needs paragraphs, link to a fuller source instead.
- Honest about ambiguity. If a term is contested (e.g. _agent_, _AGI_), say so.
- Cross-link with `<a href="#other-term">` when one definition leans on another.
- Keep entries alphabetised within their letter section. Anchors are kebab-case.

### Adding an entry

1. Find the right `<section class="letter" id="x">` in `index.html`.
2. Insert an `<article>` block in alphabetical position:

   ```html
   <article id="your-term">
     <h3>Your term <a class="anchor" href="#your-term" aria-label="link">¶</a></h3>
     <p>One to three sentences. Cross-link <a href="#related-term">related terms</a>.</p>
   </article>
   ```

3. If the term needs a new letter section that doesn't exist yet, add `<section class="letter" id="...">` and the matching link in the top `.atoz` nav.

## License

MIT. See [`LICENSE`](LICENSE).

## Inspiration

The site exists because [@dailydotdev](https://x.com/dailydotdev) tweeted on 2026-06-05:

> we need a dictionary for 'agent', 'harness', 'tool', 'context window' because AI coding invented a new dialect and shipped it before writing the docs

This is that dictionary. Suggestions for new terms can be filed as GitHub issues.
