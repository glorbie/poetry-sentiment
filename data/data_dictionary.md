# Data Dictionary

...

---

## `doc_id`

- **Type:** string
- **Description:** Synthetic ID, zero-padded.
- **Example:** `kpoem_0042`

## `text`

- **Type:** string (Korean, NFC-normalized)
- **Description:** The cleaned poem body. Original line breaks have been
  collapsed to spaces (so the text is a single line per row, suitable for
  Orange's File widget). No truncation.
- **Length stats:** mean ~247 characters, median ~228, max 543.

## `title`

- **Type:** string (Korean)
- **Description:** Poem title.
- **Example:** `서시` ("Foreword" — Yun Dong-ju's most famous poem)

