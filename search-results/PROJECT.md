# Project memory

## Goal and current status

The project contains a cross-field literature review for biology students on applications of AI in biology. As of October 14, 2026, the review selects 20 original, peer-reviewed studies first published online from January 1, 2025, through the search date. Deliverables are `literature-review.md`, `literature-review.csv`, and `search-log.txt`.

## Decisions

- Include AI methods applied to real biological data or experiments, including computational studies without new wet-lab validation.
- Cover protein engineering, genome biology, cellular analysis, and ecology without fixed subfield quotas. Health-related work qualifies when it investigates biology; purely clinical decision studies do not.
- Use the first online peer-reviewed publication date when an issue year differs. Reviews, editorials, preprints without a journal version, and passing mentions are excluded.
- Treat Crossref and publisher records as metadata checks and link claims to publisher/DOI records. Record access conservatively: only abstracts were systematically reviewed, even when more text was available.

## Verification and limitations

The CSV and search log provide the 20 selected papers, complete Crossref author lists, publication dates, DOI/source links, inclusion reasons, search terms, and near misses. PubMed rate-limited one ecology query; OpenAlex and publisher searches supplemented it. Search results were screened for relevance but not exhaustively paginated, so this is a selective review rather than an exhaustive systematic review. Full methods and results were not independently reanalyzed.

## Likely next step

For a deeper review, read the full articles, assess study quality and external validation systematically, and update the reviewed-material labels and synthesis accordingly.
