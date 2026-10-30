# Limitations

## Real behavior
Rule-based pipeline, keyword-similarity duplicate matching, factor-based scoring, and basic report workflow are implemented.

## Mocked behavior
Login, synthetic report data, landmarks, crews, and notifications are mocked.

## Not built
LLM, embeddings, image analysis, push notifications, and real account or agency integration.

## Where it can be wrong
Duplicate matching can miss paraphrases or link unrelated nearby wording. Category keywords can misclassify reports. People counts are guessed from text. Priority weights and the simplified hotspot summary are untuned demo values.
