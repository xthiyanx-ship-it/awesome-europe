# Maintenance guide

> **This file is maintained exclusively by @GeiserX.** PRs modifying it will not be accepted.

Guidelines for maintainers of this list. This guide is shared across the awesome lists ecosystem (awesome-spain + regional lists + awesome-europe). Following it ensures all repositories maintain the same quality, format, and inclusion criteria, so the collection works as a coherent whole.

## Inclusion philosophy

The fundamental criterion is: **we accept software that specifically supports the place, not software simply made by someone from the place.**

A repository is included because it interacts with institutions, services, infrastructure, regulations, or data specific to Europe. It is not enough for the author to be European or reside here. A generic JS framework created by a European developer does not belong in this list. A client for an EU institution API or an integration with European public services does.

- **Yes:** Client for EU open data portals, GDPR compliance tools, integration with European public transport APIs, EU VAT validation.
- **No:** Generic libraries created by European teams, generic software whose author simply lives in Europe.

See `AGENTS.md` (if present) for detailed criteria, edge cases, and prohibited topics.

## Reviewing PRs

1. Verify the project **specifically supports Europe** (not simply that the author is European).
2. Check the PR includes the **URL of the European service or institution** the project supports.
3. Check format: simple entry, alphabetical order, description starting with uppercase and ending with a period.
4. **CI must be green** before merging: awesome-lint-extra (format and order) + lychee (links).
5. Badges are auto-generated. Contributors only submit:
   ```markdown
   - [Name](https://github.com/owner/repo) - Brief description starting with uppercase and ending with period.
   ```
6. After merging, run the badge pipeline (if available) and push:
   ```bash
   bash scripts/gather-metadata.sh
   python3 scripts/transform-readme.py
   ```

## Adding entries as maintainer

1. Add the simple entry in the correct section, in alphabetical order.
2. Run the badge pipeline (if the repo has the scripts):
   ```bash
   bash scripts/gather-metadata.sh
   python3 scripts/transform-readme.py
   ```
3. Commit and push. Verify CI is green.
4. If the project owner hasn't been notified, open a courtesy issue on their repo:
   - Title: `Listed in awesome-europe`
   - Body: brief message explaining the inclusion and offering to remove if preferred.
   - **One issue per owner** — never open multiple issues for repos from the same user/org.

## Removing entries

Entries are not simply deleted. They are moved to `DELETED.md` in the corresponding section:

| Reason | Section in DELETED.md |
|--------|-----------------------|
| Repo archived/read-only | Archived |
| Repo deleted or renamed | Missing or renamed repos |
| Author confirmed abandonment | Abandoned |
| Does not meet inclusion criteria | Removed for not being Europe-specific |
| Superseded by another project | Replaced (link successor) |

This prevents re-additions and preserves history.

## Periodic maintenance

- **Monthly:** Review lychee output in GitHub Actions. Fix or remove broken links.
- **Quarterly:** Refresh badges (`gather-metadata.sh` + `transform-readme.py`). Check for recently archived repos:
  ```bash
  grep -oE 'https://github\.com/[^/)]+/[^/)]+' README.md | sort -u | while read url; do
    repo="${url#https://github.com/}"
    archived=$(gh api "repos/$repo" --jq '.archived' 2>/dev/null)
    [ "$archived" = "true" ] && echo "ARCHIVED: $repo"
  done
  ```

## Tools

- **awesome-lint-extra** — Custom linter. Validates format, alphabetical order, badges, and descriptions. Runs as GitHub Action (`GeiserX/awesome-lint-extra@main`) and standalone (`python3 lint.py`). Configuration in `.awesomerc.json`.
- **transform-readme.py** — Generates shields.io badges and institution/service tags from `scripts/metadata.json`.
- **gather-metadata.sh** — Fetches metadata (stars, language, license, branch) from the GitHub API for each listed repo.
- **lychee** — Link checker. Runs in CI as `lycheeverse/lychee-action@v2`. Does not block merges (`continue-on-error: true`), but results should be reviewed periodically.

## Format rules

- Description must **not start with the project name**.
- One line per entry, no line breaks.
- Descriptions in **English**.
- **Alphabetical order** within each section/subsection (case-insensitive).
- New categories: preferably with at least 3 projects.

## Prohibited content

Projects related to: pornography, NSFW, gambling, lotteries, religion, partisan politics.

## Outreach

- Open notification issues on listed projects' repos (one per owner).
- Post in relevant European developer communities after reaching critical mass.
