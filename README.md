# Summarization Comparison Report

 Overview
This project compares three summarization techniques — **Abstractive**, **Extractive**, and **Traditional NLP-based** — across two types of input texts: a narrative article and a factual news report. The goal is to identify which summarization method is most effective for different content types.


## Files Tested
- **article.txt** – Narrative-style text (story format)
- **news.txt** – Factual, structured civic report

---

## Methods Compared

### 1. Abstractive Summarization
- **Model Used**: OpenAI GPT (ChatGPT)
- **Description**: Rephrases and reconstructs sentences using semantic understanding.
- **Strengths**: Coherent, creative, fluent summaries.
- **Best Fit For**: Articles, blogs, creative writing.

### 2. Extractive Summarization
- **Models Used**: 
  - `facebook/bart-large-cnn`
  - `google/pegasus-cnn_dailymail`
- **Description**: Selects most important sentences from the source.
- **Strengths**: Preserves factual structure and terminology.
- **Best Fit For**: News, reports, technical/legal documents.

### 3. TextRank (Traditional NLP)
- **Tool Used**: `sumy` library
- **Description**: Graph-based sentence ranking using similarity/frequency.
- **Strengths**: Simple, interpretable.
- **Limitations**: Fragmented, lacks contextual understanding.

---

## Summary Output Examples

### `article.txt`

| Method      | Output |
|-------------|--------|
| **Abstractive** | “Emma’s journey took her beyond the borders... a dazzling new city filled with excitement and opportunities.” |
| **Extractive** | “Emma had always dreamed... The boat creaked and groaned but held steady.” |
| **TextRank** | “Emma dreamed of exploring. She packed a small bag...” |

 Abstractive (best coherence and narrative quality)

---

### `news.txt`

| Method      | Output |
|-------------|--------|
| **Abstractive** | “The Springfield city council meeting discussed...” |
| **Extractive** | “The city council... One major announcement was the expansion of the city’s electric bus fleet...” |
| **TextRank** | “One major announcement... environmental awareness week in September...” |

Extractive (best factual preservation and structure)

---

## 🤖 Model Behavior Comparison

- **facebook/bart-large-cnn**: More fluent, natural, ideal for presentations.
- **google/pegasus-cnn_dailymail**: Covers more factual points but less polished.
- **TextRank**: Lacks semantic rephrasing, better for basic tasks.

---

## Conclusion

| Use Case         | Recommended Approach     |
|------------------|--------------------------|
| Story/Narrative  | Abstractive (GPT-based)  |
| News/Reports     | Extractive (BART/Pegasus)|
| Simplicity/Fast  | TextRank (sumy)          |

Combining **deep learning models** with **content-specific strategy** delivers better quality, human-readable, and context-aware summaries.

---

## Tools & Libraries Used
- OpenAI GPT API
- Hugging Face Transformers (BART, Pegasus)
- Sumy (`TextRank`)
- Python, Jupyter Notebook


