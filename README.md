# Gustos-AI-Restaurant-Recommendation-System

## Project Overview

MVP proof-of-concept that analyzes 200+ Google reviews across 10 Amsterdam restaurants to provide data-driven dining recommendations. Built as a first-year CS portfolio project.

## Sentiment Analysis Evaluation

Tested three NLP libraries on real Amsterdam restaurant reviews to find the most accurate approach.

### Test Case: Mixed Sentiment Review
**Review excerpt:** "Nice atmosphere and staff. However the food was hit and miss and I ended up with food poisoning hence the one star. Long wait between each dish and quite overpriced for quality and quantity. Not a bad experience overall, but I wouldn't recommend to come for more than drinks."

**Actual rating:** ⭐ (1 star - clearly negative)

| Library | Result | Accuracy |
|---------|--------|----------|
| VADER | 0.52 (positive) | ❌ Failed |
| TextBlob | 0.28 (positive) | ❌ Failed |
| **Transformers (DistilBERT)** | **NEGATIVE (99.68% confidence)** | **✅ Correct** |

### Decision

**Chose transformers (DistilBERT)** because:
- Accurately distinguished between positive and negative reviews with mixed sentiment
- Provided strongest confidence signals (0-1 scale with percentage certainty)
- Handled sarcasm and nuanced language that rule-based approaches missed

## Tech Stack

- **Frontend:** HTML, CSS, JavaScript
- **Backend:** Python 3.14
- **NLP:** Hugging Face Transformers (DistilBERT)
- **Libraries:** VADER, TextBlob (testing only)

## Dataset

- 10 restaurants in Amsterdam
- 20 Google reviews per restaurant (200 total)
- Reviews manually collected and anonymized
- Sentiment analysis run on full review text

## Project Status

🚧 In development - MVP phase

---

*Built as a Year 1 Computer Science portfolio project*
