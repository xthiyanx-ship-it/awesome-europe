# Contributing to Awesome Europe

Thanks for your interest in contributing. This list grows thanks to the community.

## Guidelines

### Adding a project

- Make sure the project is **open source** with a public repository.
- The project must provide **support specifically for Europe** — EU institutions, regulations, standards, or cross-border infrastructure.
- The project must be **actively maintained** (activity in the last 3 years) and not archived.
- Each entry must follow the format: `- [Name](URL) - Brief description starting with a capital letter and ending with a period.`
- Add the entry in **alphabetical order** within the corresponding category.
- Check for **duplicates** and typos.
- Descriptions must be **concise and objective** (one sentence).

### Creating a new category

- Preferably with at least **3 projects** to justify it.
- Add the new category to the **table of contents** in the appropriate order.

### Entry format

```markdown
- [Name](https://github.com/owner/repo) ![Stars](https://img.shields.io/github/stars/owner/repo?style=flat-square&label=) - Description starting with a capital letter and ending with a period. ([Demo](https://example.com)) `Language` `License` `EU-Tag`
```

Each entry includes:
- **Star badge** (required): `![Stars](https://img.shields.io/github/stars/owner/repo?style=flat-square&label=)` — auto-updating shields.io badge.
- **Description** (required): One sentence, starts with a capital letter, ends with a period.
- **Demo link** (optional): `([Demo](url))` — only if a live interactive instance is available (not just a marketing page).
- **Language tag** (required if available): Backtick-wrapped primary language from GitHub, e.g. `` `Python` ``, `` `Java` ``.
- **License tag** (required if available): SPDX identifier, e.g. `` `MIT` ``, `` `Apache-2.0` ``, `` `EUPL-1.2` ``.
- **EU regulation tags** (required): One or more tags indicating which EU regulation, standard, or infrastructure the project supports. Common tags: `GDPR`, `eIDAS`, `EN16931`, `PSD2`, `VAT`, `AMLD`, `NIS2`, `DORA`, `CRA`, `AI Act`, `DSA`, `DMA`, `INSPIRE`, `Copernicus`, `FIWARE`, `CERN`, `Peppol`, `SEPA`, `CSIRT`, `EAA`, `ITS`, `Data Spaces`, `Open Data`, `eProcurement`, `CAP`, `EHDS`.

**Tag order:** Language → License → EU regulation tags (alphabetical).

Additional rules:
- Description **must not start with the project name** (awesome-lint rejects this).
- Maximum one line per entry.
- Descriptions should be in **English**.
- Run `npx awesome-lint` before submitting your PR to verify there are no errors.

### Pull requests

1. Fork the repository.
2. Create a descriptive branch (`add-project-x` or `new-category-y`).
3. Make changes following the guidelines above.
4. Submit a pull request using the provided template.
5. **Include in the PR description the URL of the EU regulation, institution, or standard** the software supports (e.g., eur-lex.europa.eu, eurostat.ec.europa.eu). This helps verify the project is relevant for Europe.

### Reporting issues

If you find broken links, archived projects, or incorrect information, open an issue describing the problem.

## Code of conduct

Be respectful and constructive. Contributions should be made in good faith and aimed at improving the list for the entire community.
