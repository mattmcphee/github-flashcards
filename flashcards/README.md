# Anki flashcards

Cards are grouped into numbered UTF-8 TSV batches of 20 to 30 notes. Each note generates one question-and-answer card. The fourth column tags each card with its [learning objective](../learning-objectives/README.md) ID.

## Note type and import settings

Create a note type named `CI-CD objectives` by cloning Anki's **Basic** note type. Use these fields in this exact order:

1. `CardId`
2. `Front`
3. `Back`

Keep a single card template. Set its front template to:

```html
{{Front}}
```

Set its back template to:

```html
{{FrontSide}}
<hr id="answer">
{{Back}}
```

Import each `.tsv` using **File > Import** in Anki desktop. Select the note type above, a destination deck, **Tab** as the separator and **Allow HTML in fields**. Map columns 1 to 3 to the fields above, and column 4 to **Tags**. The files have no header rows; the first preview row should start with a card ID such as `FC-01.01.001.01`. Check the preview before importing. If you already created the earlier six-field note type, it can keep its extra fields; update its back template as shown above and leave the extra fields unmapped.

`CardId` is the first field so importing a corrected batch can update matching notes without changing their identity. Choose matching by note type and update existing notes; do not import duplicates as new notes. Keep the same note type across batches. Set the browser sort field to `Front` if desired.

## Content notes

Architecture and scenario answers are design judgements, not claims that a vendor mandates that design. Product-specific answers name their platform; Azure DevOps answers concern Services unless explicitly qualified. Recheck changing product behaviour before using these cards as operational instructions.

Cards use HTML for code. No media files, add-ons or reverse-card templates are required. Objective ID tags are metadata, not part of the recall prompt.

Text import requirements: [Anki manual](https://docs.ankiweb.net/manual/importing/text-files), accessed 2026-11-16.

## Batch index

710 cards cover all 665 learning objectives. Import batches in any order after creating the note type above. The two batches in each row together cover that section. See the [verification record](verification.md) for checks and limits.

| Section | Objectives covered | Cards | Batch 1 | Batch 2 |
| --- | ---: | ---: | --- | --- |
| 1. CI/CD fundamentals | 31 | 40 | [20 cards](01-batch-01.tsv) | [20 cards](01-batch-02.tsv) |
| 2. Source control and repository governance | 30 | 40 | [20 cards](02-batch-01.tsv) | [20 cards](02-batch-02.tsv) |
| 3. GitHub Actions | 53 | 60 | [30 cards](03-batch-01.tsv) | [30 cards](03-batch-02.tsv) |
| 4. Azure DevOps and Azure Pipelines | 58 | 60 | [30 cards](04-batch-01.tsv) | [30 cards](04-batch-02.tsv) |
| 5. Pipeline engineering and scripting | 40 | 41 | [21 cards](05-batch-01.tsv) | [20 cards](05-batch-02.tsv) |
| 6. Identity and secrets management | 36 | 40 | [20 cards](06-batch-01.tsv) | [20 cards](06-batch-02.tsv) |
| 7. Runner and pipeline security | 45 | 45 | [23 cards](07-batch-01.tsv) | [22 cards](07-batch-02.tsv) |
| 8. Software supply-chain security | 46 | 47 | [24 cards](08-batch-01.tsv) | [23 cards](08-batch-02.tsv) |
| 9. Testing and quality engineering | 37 | 40 | [20 cards](09-batch-01.tsv) | [20 cards](09-batch-02.tsv) |
| 10. Artifacts, dependencies and versioning | 36 | 40 | [20 cards](10-batch-01.tsv) | [20 cards](10-batch-02.tsv) |
| 11. Deployment strategies and release management | 42 | 42 | [21 cards](11-batch-01.tsv) | [21 cards](11-batch-02.tsv) |
| 12. Infrastructure as Code and GitOps | 38 | 40 | [20 cards](12-batch-01.tsv) | [20 cards](12-batch-02.tsv) |
| 13. Enterprise governance and compliance | 48 | 48 | [24 cards](13-batch-01.tsv) | [24 cards](13-batch-02.tsv) |
| 14. Monitoring, reliability and troubleshooting | 47 | 47 | [24 cards](14-batch-01.tsv) | [23 cards](14-batch-02.tsv) |
| 15. Developer experience and platform engineering | 39 | 40 | [20 cards](15-batch-01.tsv) | [20 cards](15-batch-02.tsv) |
| 16. Advanced enterprise scenarios and architecture | 39 | 40 | [20 cards](16-batch-01.tsv) | [20 cards](16-batch-02.tsv) |

