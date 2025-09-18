# Monk-GPT

**A philosophical AI trained on Advaita Vedanta using Transformer-based self-attention, embeddings, and retrieval-augmented generation.**

## Project Overview
Monk-GPT is a scholarly AI assistant specialized in Advaita Vedanta. It explains key concepts, translates Sanskrit verses, and provides concise commentarial insights grounded in canonical sources. The model uses embeddings and self-attention (Transformer architecture from *"Attention Is All You Need"*) to generate faithful, philosophically rigorous outputs.

## Mission
Create a philosophical AI trained on Advaita Vedanta that uses text, embeddings, and self-attention to provide faithful explanations, translations, and commentaries while respecting the canonical sources and multiple scholarly interpretations.

## Primary Users
- Students (beginner → intermediate) seeking clear philosophical explanations  
- Scholars needing precise citations and careful exegesis  
- Curious readers seeking reliable, worldview-sensitive summaries

## High-Level Scope
- Explain core Advaita Vedanta concepts (e.g., Tat Tvam Asi, Maya, Neti-Neti)  
- Provide literal translations of short Sanskrit verses (user-provided or public-domain)  
- Offer concise commentaries with source citations  
- Use embeddings + Transformer self-attention with retrieval-augmented generation (RAG) to reduce hallucinations  
- Distinguish original text, translation, and interpretation  
- Present alternative scholarly views when relevant

## Out of Scope
- Medical, legal, or financial advice  
- Promoting violence, hatred, or illegal activity  
- Replacing a qualified teacher for rituals or initiation  
- Publishing modern copyrighted translations without permission

## Ethics & Safety
- If uncertain, respond: "I don't know for certain" and provide sources to check  
- Present multiple scholarly views when available and cite authors  
- Refuse misuse of scripture to justify harm; avoid proselytizing

## Minimum Viable Dataset for Prototype
- Public-domain Sanskrit canonical texts (Upanishads, Bhagavad Gita text, Brahma-Sutras)  
- User-created or public-domain commentaries  
- Chunked text indexed via embeddings for retrieval  
*(Modern translations added only with explicit licensing.)*

## Success Criteria
- Prototype: model answers 20 held-out questions with ≥80% alignment to retrieved sources (automated retrieval-to-output match)  
- Human evaluation: 2 scholars rate 30 outputs — average ≥4/5 for faithfulness & tone

## Repository Structure
monk-gpt/
├─ data/
│ ├─ raw/ # Canonical texts and public-domain commentaries
│ ├─ processed/ # Cleaned, tokenized, chunked data
│ └─ manifest.csv # Metadata for texts and translations
├─ notebooks/ # Data audits, experiments
├─ src/
│ ├─ preprocess.py # Data cleaning & chunking
│ ├─ build_index.py# Embeddings & FAISS index
│ └─ train_lora.py # LoRA/PEFT fine-tuning
├─ infra/
│ └─ train_configs/
├─ eval/ # Test sets, human evaluation instructions
├─ .gitignore
├─ LICENSE
└─ README.md


## Getting Started
1. Populate `data/raw/` with canonical texts (Sanskrit + public-domain commentaries)  
2. Update `data/manifest.csv` with metadata for each text  
3. Run `src/preprocess.py` to produce cleaned, chunked data  
4. Run `src/build_index.py` to create the embedding index  
5. Use `src/train_lora.py` for initial instruction-tuning experiments  

## License
MIT License — see LICENSE file  

## Contact
Deo Rejan
