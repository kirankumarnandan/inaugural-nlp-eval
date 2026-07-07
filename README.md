# inaugural-nlp-eval
# Inaugural Speech NLP Analysis & Evaluation Framework

Comparative NLP analysis of all 58 US presidential inaugural speeches (1789–2021), covering TF-IDF, topic modeling, sentiment, and rhetorical style.

## Status
🚧 In progress

## Goal
Started as a TF-IDF learning project on 3 speeches. Expanded to the full corpus, then reworked as an evaluation framework — comparing classic NLP methods (TF-IDF, keyword-based themes, TextBlob sentiment) against modern methods (sentence embeddings, BERTopic, transformer sentiment, LLM-as-judge) with human-labeled ground truth.

## Roadmap
- [x] v1: Baseline pipeline on full 58-speech corpus (TF-IDF, TextBlob, keyword themes)
- [ ] v2: Modern methods (spaCy, BERTopic, transformer sentiment, sentence embeddings)
- [ ] v3: Evaluation framework — human-labeled ground truth + LLM-as-judge comparing v1 vs. v2 methods

## Structure
