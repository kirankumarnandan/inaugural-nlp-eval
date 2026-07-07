# Evaluation Plan

## What v1 got wrong (hypotheses to test, not yet proven)
- TF-IDF top-terms: may surface noise words, not distinctive ones
- Themes: keyword dictionary is author-biased, not data-driven
- Sentiment: TextBlob gives one score per speech — no granularity

## What "better" will be measured against
1. Similarity: 20 hand-picked speech pairs, human 1-5 similarity rating
2. Sentiment: 30 sampled sentences, human pos/neu/neg label
3. Themes: 5 speeches, human ranking of theme prominence

## Methods to compare (v1 baseline vs. v2 candidates)
| Task | v1 (baseline) | v2 candidate(s) |
|---|---|---|
| Similarity | TF-IDF cosine | sentence-transformer embeddings |
| Themes | keyword dictionary | BERTopic, LLM zero-shot |
| Sentiment | TextBlob (doc-level) | transformer (sentence-level) |

## Success metric per task
- Similarity: Spearman correlation vs. human labels
- Sentiment: accuracy / F1 vs. human labels
- Themes: topic coherence score + human agreement %

## Not yet decided (revisit in Session 5)
- LLM judge model choice
- Exact wording of judge prompts
