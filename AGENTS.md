# Agent instructions

## Purpose and scope

This repository contains study material for CI/CD, GitHub Actions, Azure DevOps, and related enterprise engineering practices. It holds a topic map, learning objectives, and Anki flashcards. It does not currently contain application code or a build system.

- Read `README.md` and the relevant parts of `topic-map.md` before changing study material.
- Treat `topic-map.md` as the source of truth for topic scope, hierarchy, and numbering.
- Store learning objectives in `learning-objectives/` and flashcard sources, supporting media, and exported decks in `flashcards/`.
- Use topic numbers in related filenames, following the convention in `README.md`.

## Make focused changes

- Make the smallest change that satisfies the request. Preserve unrelated content and user edits.
- A formatting or reorganisation request does not authorise adding new study content.
- Do not expand the topic map or renumber topics unless the requested work calls for it. When renumbering, update affected references and filenames together.
- Follow existing conventions. State material assumptions, and ask for clarification when an unresolved choice would change the requested scope or meaning.
- Do not add dependencies, generators, CI workflows, or other tooling without a concrete need in the requested work.

## Technical accuracy and sources

- Verify unfamiliar or uncertain technical claims against primary sources, preferably official documentation.
- Check current official documentation for facts that can change, including product capabilities, permissions, security behaviour, limits, pricing, and licensing.
- Distinguish GitHub Actions from Azure Pipelines behaviour. Include relevant platform, version, hosting, or licence conditions rather than implying a rule applies everywhere.
- Keep source links with the relevant learning objectives or card source material so claims can be checked later. Record an access date when a claim depends on current product behaviour.
- Do not invent commands, configuration options, citations, or validation results. Flag unresolved uncertainty instead of presenting it as a fact.
- Use fictional values in examples and keep credentials and personal data out of the repository.

## Learning objectives

- Align each objective with an existing topic or subtopic and include its topic number.
- Describe an observable outcome using verbs such as explain, compare, configure, diagnose, or design. Avoid vague outcomes such as "understand" or "be familiar with".
- Keep objectives focused and assessable. Separate outcomes that require different knowledge or skills.
- Check existing objectives before adding new ones to avoid duplicates and conflicting guidance.

## Flashcards

- Give every card one or more active objective IDs in its `LearningObjectiveIds` metadata field, following the ID stability and reference rules in `learning-objectives/README.md`.
- Test one focused idea per card. Split broad questions and long lists into smaller prompts where practical.
- Make prompts unambiguous and understandable during shuffled review. Name the platform or context when it affects the answer.
- Keep answers concise while retaining conditions needed for correctness. Avoid trivia and trick questions that do not support an objective.
- Use scenarios and comparisons when they help test application or judgement rather than recognition alone.
- Preserve the established note types, field order, identifiers, and tagging conventions. When introducing a card format, document its fields and Anki import settings before producing a large batch.
- Keep editable text sources alongside deck exports where possible. Do not hand-edit binary Anki packages or local collection databases.
- Preserve meaningful tabs, empty fields, escaping, and media references in card source files.

## Writing and formatting

- Use clear, plain language and Australian English, consistent with the existing topic map. Preserve official product names and exact code identifiers.
- Use sentence case headings, a consistent Markdown hierarchy, and blank lines around headings and lists.
- Avoid em dashes and en dashes in prose and headings. Use commas, colons, parentheses, or separate sentences as appropriate.
- Format commands, configuration keys, event names, filenames, and other literal identifiers as inline code or fenced code blocks.
- Follow `.editorconfig` and `.gitattributes`, including UTF-8 encoding and LF line endings.

## Verify before finishing

- Review the diff for unintended changes, missing content, duplicate material, and inconsistent terminology.
- For structural changes, check heading levels, topic numbering, internal links, and affected cross-references.
- For objective or card changes, check alignment, technical accuracy, clarity, and source links.
- For card files, check field counts against the documented format and confirm referenced media exists. When an Anki import or export check is relevant and available, perform it; otherwise state that it was not verified in Anki.
- Use checks appropriate to the change. Do not introduce a test framework for documentation edits.
- Summarise what changed, what was checked, and any remaining uncertainty. Only claim checks that were actually performed.
