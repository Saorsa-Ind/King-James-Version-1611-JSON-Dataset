# King James Version (1611) — JSON Dataset

A public-domain, machine-readable dataset of the **1611 King James Version (KJV) Bible**, including the Old Testament, New Testament, and Apocrypha.

The text is organized by book, chapter, and verse in JSON format. It is provided by **Saorsa Industries** for anyone to use, adapt, analyze, or incorporate into their own projects, for any purpose.

## Contents

The repository includes **81 book files** and **36,807 verse records**. The Letter of Jeremiah is provided as a separate book from Baruch.

```text
├── books/
│   ├── Genesis.json
│   ├── Exodus.json
│   ├── ...
│   ├── Baruch.json
│   ├── LetterofJeremiah.json
│   └── Revelation.json
├── books.json
└── books_chapter_count.json
```

- **`books/`** — One JSON file per book, containing its chapters and verses.
- **`books.json`** — Ordered list of book names.
- **`books_chapter_count.json`** — Book names and their chapter counts.

## JSON Format

Each book file follows this structure (example abridged):

```json
{
  "book": "Genesis",
  "chapter-count": "50",
  "chapters": [
    {
      "chapter": 1,
      "verses": [
        {
          "verse": 1,
          "text": "In the beginning God created the Heauen, and the Earth."
        }
      ]
    }
  ]
}
```

The `chapter-count` field is a string; chapter and verse numbers are integers. Text retains historical spelling and punctuation found in this dataset rather than being modernized.

## Example Usage

Read a book and print its first verse using Python:

```python
import json

with open("books/Genesis.json", encoding="utf-8") as file:
    genesis = json.load(file)

print(genesis["chapters"][0]["verses"][0]["text"])
```

No additional Python packages are required.

## Potential Uses

This dataset may be used for **any purpose**, including Bible applications, reading tools, search engines, concordances, textual comparison, linguistics, natural language processing (NLP), machine learning, semantic search, digital humanities, educational resources, and other research or software projects. These are examples, not restrictions.

## Public Domain

The 1611 King James Version text is in the public domain in the United States. The dataset is provided for unrestricted reuse; no permission from Saorsa Industries is required. Users outside the United States should verify any applicable local rules, including those concerning the Authorized Version in the United Kingdom.

Attribution is appreciated but not required.

## Maintainer

**Saorsa Industries**  
https://saorsaindustries.com
