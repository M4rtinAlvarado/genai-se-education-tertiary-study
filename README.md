# Teaching Software Engineering with Generative AI — Supplementary Material

Supplementary material [S] for the paper **"Teaching Software Engineering with Generative AI: Connecting
SWEBOK, Cognitive Processes, and Didactic Techniques"**.

Martín Alvarado, Claudia Vergara, Martín Maza, Juan Salazar-Fernandez
([0000-0001-7200-0614](https://orcid.org/0000-0001-7200-0614)) and Valeria Henríquez
([0000-0002-9003-2254](https://orcid.org/0000-0002-9003-2254)) — Instituto de Informática, Universidad
Austral de Chile. Funded by ANID FONDECYT Iniciación 11260438.

## Contents

| | |
|---|---|
| [`METHODOLOGY.md`](METHODOLOGY.md) | Detailed methodology: search string and filters, selection criteria, extraction and coding rules, tools and versions, human verification, deviations from the initial protocol, threats to validity |
| [`prompts/`](prompts/) | The prompts used with each LLM, verbatim |
| [`figures/`](figures/) | Figures 1–3 of the paper |
| [`included_studies/`](included_studies/) | The 33 reviews (`reviews.csv`, with the 10 snowballing seeds marked) and the primary studies (`primary_studies.csv`) |
| [`results/`](results/) | Complete map of practices: SWEBOK Knowledge Area × UnADM didactic technique × cognitive level, for the reviews and the primary studies, with the supporting quote for each practice |
| [`PRISMA-trAIce.md`](PRISMA-trAIce.md) | Checklist for reporting the use of AI in the review |

## Study in brief

1. Search in OpenAlex (2023–2026): 90 records.
2. Selection of reviews: 40 after title and abstract screening, 38 full texts, 33 reviews after an
   LLM-assisted relevance rating.
3. Data extraction from the 33 reviews with Claude Sonnet 5, every item supported by a verbatim quote.
4. Backward snowballing from 10 seed reviews: 113 candidates, 102 full texts, 101 primary studies.
5. Coding of each GenAI-supported practice in the primary studies with NotebookLM, validated by script
   against the controlled vocabularies and the PDF text.

The full texts of the analyzed studies are not included, since they are copyrighted; every study is
identified by DOI or full reference in `included_studies/`.

## License

CC BY 4.0 (see [`LICENSE`](LICENSE)). Cite as indicated in [`CITATION.cff`](CITATION.cff).
