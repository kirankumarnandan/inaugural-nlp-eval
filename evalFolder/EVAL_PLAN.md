# Evaluation Plan

## What v1 got wrong (hypotheses to test, not yet proven)
- Similarity heatmap unreadable at 58x58 — need embeddings + subset comparison to make similarity findings legible
- max_features=700/500 in TfidfVectorizer is an arbitrary cap carried over from the 3-speech version, not min_df/max_df based — likely dropping meaningful terms
- Charts indexed by president name, not year — duplicate labels for multi-term presidents (FDR, Washington), no visible time trend
- Keyword theme dictionary may misfire on era-specific words (e.g. "danger"/"crisis" scoring generically high for old speeches unrelated to modern crises like COVID) — needs spot-checking against BERTopic output later

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
