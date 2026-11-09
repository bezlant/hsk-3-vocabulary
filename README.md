# HSK 3.0 vocabulary lists

Machine-readable vocabulary lists for HSK 3.0, the nine-level standard that replaces the old six-level HSK. CSV and JSON, one row per word: simplified, traditional, pinyin, level, English definitions.

The word scope follows the final 新版HSK考试大纲 published by the Center for Language Education and Cooperation in November 2025. These are the same lists behind the vocabulary pages, PDFs and Anki decks on [hskstory.com](https://hskstory.com).

## Counts

The official syllabus numbers 11,000 vocabulary entries cumulatively. Repeated written forms account for most of the gap to the counts below.

| Level | Official cumulative entries | Cleaned cumulative items | Introduced at this level |
|-------|----------------------------|--------------------------|--------------------------|
| HSK 1 | 300 | 300 | 300 |
| HSK 2 | 500 | 496 | 197 |
| HSK 3 | 1,000 | 988 | 493 |
| HSK 4 | 2,000 | 1,978 | 990 |
| HSK 5 | 3,600 | 3,557 | 1,579 |
| HSK 6 | 5,400 | 5,334 | 1,777 |
| HSK 7-9 | 11,000 | 10,896 | 5,562 |

HSK 7, 8 and 9 share one vocabulary band in the syllabus, so they share one file here.

## Files

| File | Contents |
|------|----------|
| `hsk-3.0-vocabulary.csv` / `.json` | 10,898 rows, one per distinct word, with the level that introduces it |
| `by-level/hsk-1` through `by-level/hsk-7-9` | the words each level introduces (300, 197, 493, 990, 1,579, 1,777, 5,562) |
| `hsk-2.0-to-3.0-changes.csv` / `.json` | 11,087 rows, one per word in either standard, with its old level, new level and what changed |

Columns are `simplified`, `traditional`, `pinyin`, `level`, `definitions`. In CSV, multiple definitions are joined with `; `; in JSON they are an array. Pinyin is the citation reading with tone marks, before tone sandhi. The change list uses `simplified`, `hsk_2_level`, `hsk_3_level`, `status`, where status is one of `added`, `removed`, `same_level`, `moved_up`, `moved_down`.

Filter the combined file by `level` for a cumulative list. Two words make those counts one short of the sum: 有点儿 and 有时 appear in the HSK 1 and HSK 2 files but not in the higher ones, where the syllabus stores them as 有一点儿 and 有时候.

## How the lists were cleaned

The official PDF numbers its entries cumulatively and repeats written forms across levels. Getting to one row per word means deduplicating those repeats and normalizing variant spellings, which puts the cleaned totals slightly below the official entry counts. The per-level files come from comparing adjacent cumulative lists as sets, so they are not simple subtractions of the official totals.

[Complete HSK 3.0 Vocabulary List](https://hskstory.com/guides/hsk-30-vocabulary-complete) walks through the cleaning and lists the discrepancies level by level.

## Sources and attribution

- Word scope and levels: the final HSK examination syllabus (新版HSK考试大纲), 中外语言交流合作中心 / Center for Language Education and Cooperation, November 2025, quoted from the [Chinese Test Service Website](https://www.chinesetest.cn/syllabus) (www.chinesetest.cn). Its level system follows 《国际中文教育中文水平等级标准》 (GF 0025-2021), 教育部 and 国家语言文字工作委员会, 2021.
- Pinyin and English definitions: [CC-CEDICT](https://www.mdbg.net/chinese/dictionary?page=cedict), used under CC BY-SA 4.0, with per-word edits and a few entries written by HSKStory for words CC-CEDICT lacks.
- Traditional forms: CC-CEDICT, with OpenCC conversion for the nine words it does not cover.

All rights in the syllabus and in GF 0025-2021 stay with their publishers. This repository holds extracted words, levels and readings only. It does not reproduce the syllabus PDF, its layout, or CTI and 汉考国际 branding, and nothing here is an official product of CTI, CLEC or 教育部.

## License

[CC BY-SA 4.0](LICENSE). CC-CEDICT is share-alike, so anything derived from these files carries the same license. Attribute HSKStory and CC-CEDICT.

The words, levels and readings themselves are facts about a published standard, and HSKStory claims no copyright in them.

## Citation

```bibtex
@misc{hskstory_hsk3_vocabulary,
  title  = {HSK 3.0 Vocabulary Lists},
  author = {HSKStory},
  year   = {2026},
  url    = {https://github.com/bezlant/hsk-3-vocabulary},
  note   = {CC BY-SA 4.0}
}
```

## Corrections

Open an issue with the word and what is wrong. Definition fixes that belong upstream are better sent to CC-CEDICT, which both this dataset and the site follow.

---

Made by HSKStory — graded Chinese stories for HSK 1–9 ([hskstory.com](https://hskstory.com)).
