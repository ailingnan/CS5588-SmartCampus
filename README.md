# CS5588-SmartCampus
CS5588 Group Project
# A Trust-Aware Multimodal GenAI Digital Twin for UMKC Campus Information & Decision Support

## Team Name
**Group 2**

## Team Members
- **Lyza Iamrache** — (https://github.com/LyzaIamrache)  
- **Ailing Nan** — https://github.com/ailingnan (Primary Contact)  
- **Gia Huynh** — [GitHub](#)  

---

## Problem Statement
UMKC students and visitors face difficulty accessing reliable and up-to-date campus information—such as navigation, shuttle schedules, parking, or academic policies—because existing resources are fragmented (PDFs, websites, tables) and standard chatbots may generate plausible but unsupported answers.  

This project develops a **GenAI-driven multimodal digital twin** that provides evidence-backed, trustworthy, and actionable answers. The system integrates text, tables, and images, enforces citation of authoritative documents, and can refuse to answer when information is missing, supporting **decision-oriented workflows**.

---

## High-Level GenAI System Architecture
1. **Data Ingestion & Knowledge Layer**  
   - PDFs (student handbook, parking permits, shuttle schedules, catalogs)  
   - Campus maps  
   - OCR + chunking + metadata + provenance tracking  

2. **Retrieval & Grounded Generation (RAG)**  
   - Sparse (BM25) + dense (FAISS embeddings) retrieval  
   - Hybrid fusion, optional reranking  
   - Grounded generation with evidence citation or refusal  

3. **Scenario Reasoning & Digital Twin Simulation**  
   - Short-horizon decision support (e.g., shuttle feasibility, academic planning)  
   - Rule-constrained LLM reasoning  

4. **Interface & Human-in-the-Loop**  
   - Interactive notebook showing retrieved evidence, citations, and refusal messages  

---

## Datasets
- [UMKC University Catalog 2025–2026](https://catalog.umkc.edu/pdf/2025-2026%20University%20Catalog_Archived%209-10-25.pdf) — Academic programs, course requirements, policies  
- [UMKC Campus Maps](https://www.umkc.edu/documents/umkc-health-sciences-campus-map.pdf) & [Volker Map](https://www.umkc.edu/documents/umkc-volker-campus-map.pdf) — Building layouts, paths, landmarks  
- [Shuttle Schedule](https://www.umkc.edu/transportation/docs/2026-spring-shuttle-schedule.pdf) — Timetable data for routes and stops  
- [Parking Permits](https://www.umkc.edu/parking/parking-options/student-permits.html) — Lot availability, cost, permit types  
- [Student Handbook](https://www.umkc.edu/student-affairs/docs/umkc-student-handbook.pdf) — Policies, rules, procedures  
- [Visual Identity Guidelines](https://www.umkc.edu/mcom/docs/visual-identity-guidelines.pdf) — Logos, color schemes, design rules  
- [Campus Crime Report (Clery)](https://www.umkc.edu/police/docs/2025ccfsr.pdf) — Crime statistics, tables, figures  

---

## Related Papers
- **[GFM-RAG: Graph Foundation Model for RAG](https://doi.org/10.48550/arXiv.2502.01113)** — Graph-based retrieval for structured reasoning  
- **[KnowTrace: Iterative RAG](https://doi.org/10.1145/3711896.3737015)** — Iterative refinement of retrieved context  
- **[Multi-Stage Verification-Centric Multimodal RAG](https://github.com/Breezelled/KDD-Cup-2025-Meta-CRAG-MM)** — Minimizing hallucination and enforcing evidence verification  

---

## Deliverables
- Fully versioned GitHub repository with code, prompts, datasets, and evaluation scripts  
- Working multimodal GenAI prototype for UMKC campus information  
- Phase 1: Interactive notebook for retrieval and grounding demonstration  
- Technical report describing architecture, experiments, evaluation, and lessons learned

