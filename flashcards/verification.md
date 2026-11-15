# Verification record

Reviewed on 2026-11-16.

## Content review

Cards were checked against primary documentation and reference material during drafting. Review focused on platform distinctions, trust boundaries, exact configuration identifiers, and conditions that make an answer valid. Scenario answers express reasoned design choices; they are not universal vendor requirements. Source links and review dates were removed from the TSV files when the import format was reduced to four columns.

Examples of details checked against current documentation include GitHub token-triggered workflow exceptions, environment reviewer behaviour, ephemeral runner cleanup, Azure pipeline resource checks, workload identity federation, SLSA v1.2 build levels, and current DORA terminology. Cards avoid treating changing prices, plan entitlements or limits as universal constants.

The review corrected outdated source URLs before the metadata columns were removed and preserved the literal GitHub event name `synchronize`. The earlier link check found that all 173 source URLs used during drafting returned HTTP 200.

## File and coverage checks

| Check | Result |
| --- | --- |
| Active objective IDs in the source catalogue | 665 |
| Objective IDs represented by cards | 665 |
| Missing or unknown objective references | 0 |
| Cards | 710 |
| TSV batches | 32 |
| Cards per batch | 20 to 30 |
| Duplicate card IDs or identical prompts | 0 |
| Fields per data row | 4, all populated |
| Encoding and line endings | Valid UTF-8, LF, final newline |
| Prompt and answer HTML | Parsed successfully |
| Objective ID tag | Present on every card |
| TSV parser round trip | Row counts preserved |

Each card carries its objective ID as a tag, so coverage can be traced directly from the TSV files. Representation means each objective has at least one relevant recall or application prompt. Broad design and implementation objectives still benefit from hands-on practice.

## Anki import check

The separator, field mapping and duplicate-update approach were checked against the [Anki text import manual](https://docs.ankiweb.net/manual/importing/text-files). Header lines were removed because an import preview treated them as card data. The required note type and templates are documented in [README.md](README.md).

An actual import into an isolated Anki collection has not been performed. Import requires the one-time note type setup described in the guide. These files contain one note and one card per data row, with no media dependencies.
