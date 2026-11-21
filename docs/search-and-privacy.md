# Search and privacy

[Back to README](../README.md) · [简体中文](./search-and-privacy.zh-CN.md)

## Find a file, even when the name escapes you

Nearkeep returns filename and keyword matches first. When appropriate, local semantic retrieval adds relevant passages from supported documents. For example, a description of late-payment obligations can surface payment clauses when their text is available. Check the original document before relying on a result.

The package includes **Qwen3-Embedding-0.6B Q8_0**, running through a local llama.cpp runtime. This is a retrieval model; it does not generate chat replies or summaries.

## Supported content

| Content | Current coverage |
| --- | --- |
| PDFs with a text layer | Text extraction and retrieval |
| TXT, Markdown, CSV, TSV, JSON, LOG | Text extraction and retrieval |
| Scanned PDFs | Full OCR is not provided |
| Office documents and other formats | Body-text retrieval is not provided |

Large or long documents and processing limits can produce partial coverage. A cold model start may take tens of seconds. Ordinary search remains available when the model is busy or unavailable. Search history is stored locally and supports deleting individual entries.

Importing a file, previewing it and searching its contents are separate capabilities: a file you can keep in the Library may not support content search.

## What stays local

Current file management, indexing and model retrieval run on your computer. Document text is not sent to cloud AI. OS security checks, email feedback and external content you choose to open may use the network.

Comprehensive offline and network-traffic audits are not complete. Local processing should not be read as a guarantee of complete offline operation in every scenario or absolute security.

Online accounts, cloud sync, generative Q&A and summaries are not currently available. Keep an independent backup of important files; a local Library is not a backup service.
