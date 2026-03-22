# AGENTS.md — awesome-europe

## Purpose

A curated list of open source software that provides **support specifically for Europe** — its institutions, regulations, standards, and cross-border infrastructure. All content in English. The focus is pan-European: software must target a significant portion of European countries, not just one or two.

## Inclusion criteria

### Include

- Software that interacts with **EU/European institutions** (European Commission, ECB, Eurostat, EBA, ESMA, ENISA, ERA, EFSA, EEA, Europol, Eurojust, etc.).
- Implementations of **EU regulations and directives** (GDPR, eIDAS, PSD2, NIS2, EU AI Act, DMA, DSA, MiCA, DORA, European Accessibility Act, etc.).
- Tools for **EU-wide standards** (SEPA, Peppol, EN 16931, INSPIRE, ETCS, CE marking, EN 301 549, etc.).
- Software for **pan-European data systems** (Eurostat, EU Open Data Portal, Copernicus, Galileo, ENTSOE Transparency Platform, EUR-Lex, ECLI, etc.).
- Cross-border **digital infrastructure** (eIDAS digital identity, EU Digital Identity Wallet, EU Digital COVID Certificate, EHIC, Erasmus systems, etc.).
- **EU VAT, customs, and trade** tools (VIES, OSS/IOSS, TARIC, CN codes, EU customs systems, Intrastat).
- **Pan-European energy** systems (ENTSO-E, ACER, EU ETS, REMIT).
- Software that explicitly targets **multiple European countries** as its primary scope (e.g., "works across all EU member states").

### Do not include

- Software specific to a **single country** — that belongs in country-specific awesome lists (awesome-spain, awesome-germany, etc.).
- Software that targets only **2-3 countries** or a small regional cluster, unless implementing an EU-wide standard.
- **Global software** that happens to work in Europe among many other regions (e.g., generic payment processors, global tax tools).
- Software by European developers that has **no Europe-specific functionality** (generic JS frameworks, visualization libraries, etc.).
- **NATO or military** software.
- Software only tangentially related to Europe (e.g., a global mapping tool that includes European map tiles).

### Grey area — use judgement

- Software targeting the **EEA** (EU + Norway, Iceland, Liechtenstein) or **EU + UK + Switzerland** — generally include, as these countries follow most EU regulations.
- Projects that started as EU-specific but went global — include if European functionality remains a distinct, prominent feature.
- Software for **EU candidate countries** implementing EU acquis — include if specifically about EU alignment.

## Entry format

```markdown
- [Name](https://github.com/owner/repo) - Description starting with a capital letter and ending with a period.
```

- Description **must not start with the project name**.
- Maximum one line per entry.
- Validate with awesome-lint: `npx awesome-lint`.

## Verification before adding

Before including a repository, check:

- **Exists and is public**: the GitHub link works and the repo is not private.
- **Not archived or read-only**: if archived, it goes to `DELETED.md` ("Archived" section).
- **Reasonable activity**: at least one commit in the last 3 years, unless it's a stable/complete project.
- **Not a duplicate**: cross-check with `README.md` and `DELETED.md`.
- **Minimum quality**: has basic documentation (README) and is not an empty or test repository.

## Pull requests and contributions

- PRs should use the template in `.github/PULL_REQUEST_TEMPLATE.md`.
- **Required**: include in the PR the **URL of the EU regulation, institution, or standard** the software supports (e.g., eur-lex.europa.eu, eurostat.ec.europa.eu).
- Issue templates available for suggesting projects (`suggest-project.md`) and requesting removal (`remove-project.md`).

## Structure

- Sections with `##`, subsections with `###`.
- Table of contents at the top between `<!--lint disable/enable awesome-list-item-->` comments.
- At the end: Contributing section, Note, and Disclaimer.

## Prohibited topics

No projects related to: pornography, NSFW content, gambling, religion, partisan politics.

## Promotion

- Notify repo owners by opening an issue titled "Listed on awesome-europe" with a brief English message offering to remove if preferred.
- Post to European dev communities (Reddit r/europe, r/programming, Hacker News) after reaching critical mass.
- Submit to sindresorhus/awesome after 30 days from repo creation.

## Git

- Identity: `GeiserX` / `9169332+GeiserX@users.noreply.github.com`
- No `Co-Authored-By` in commits.
- No attribution to Claude/Anthropic in public text.
- Default branch: `main`.
- Always `unset GITHUB_TOKEN` before `gh` commands.
