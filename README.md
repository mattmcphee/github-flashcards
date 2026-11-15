# GitHub flashcards

A study collection covering CI/CD, GitHub Actions, Azure DevOps, and related enterprise engineering practices. The repository holds the topic map, learning objectives, and Anki flashcards.

## Repository layout

| Path | Purpose |
| --- | --- |
| [topic-map.md](topic-map.md) | Topic hierarchy and study scope. |
| [learning-objectives/](learning-objectives/README.md) | Indexed learning objectives with stable IDs for flashcard references. |
| [flashcards/](flashcards/) | Anki flashcard source files, supporting media, and exported decks. |

The learning objectives cover every topic bullet in the map. All 665 objectives are represented by 710 flashcards in 32 batches of 20 to 30 cards. See the [Anki import instructions and batch index](flashcards/README.md).

## Adding study material

1. Use the topic map to choose a topic and its section number.
2. Find the relevant objectives in the [learning objective index](learning-objectives/README.md), adding or refining objectives when needed.
3. Create flashcards in `flashcards/` and reference one or more active objective IDs in each card's `LearningObjectiveIds` metadata field.
4. Check each card for accuracy and keep each question focused on one idea.

Use topic numbers in filenames to connect related material, for example `01-cicd-fundamentals.md` for objectives and `01-cicd-fundamentals.tsv` for card source files.

Keep editable card sources alongside exported Anki decks where possible. UTF-8 tab-separated text (`.tsv`) is a suitable source format for review in Git. Anki deck packages (`.apkg`) can also be committed. Local Anki collection databases and their temporary files are ignored.

## Editing conventions

- Write documentation and objectives in Markdown.
- Keep headings and topic numbers consistent with the topic map.
- Use UTF-8 encoding and LF line endings for text files.
- Keep supporting media with the relevant flashcards.

No build step or dependency installation is required to edit the study material.
