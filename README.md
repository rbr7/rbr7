<h1 align="center">Hi, I'm Rohan 👋</h1>

<p align="center">
  <b>Scalable Machine Learning · Foundation models · Explainable AI · Clinical NLP &amp; Text Mining · Healthcare Data Quality </b><br>
                                                         <p align="center">
  <b>LLMs  |  OpenClaw  |  RL  |  Python  |  R  |  Scala  |  Spark</b><br>
  
  Senior Data Scientist and applied AI researcher at Massachusetts General Hospital (under MGB Inc.) -> turning messy, multi-modal, cross-sites healthcare &amp; multi-omics data into validated, model-ready assets, then building interpretable ML and LLM systems that domain experts can trust.
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/rohan-bhukar/"><img src="https://img.shields.io/badge/LinkedIn-rohan--bhukar-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="https://scholar.google.com/citations?user=6RGIV64AAAAJ&hl=en"><img src="https://img.shields.io/badge/Google%20Scholar-Publications-4285F4?style=for-the-badge&logo=googlescholar&logoColor=white" alt="Google Scholar"></a>
  <a href="https://github.com/rbr7"><img src="https://img.shields.io/badge/GitHub-rbr7-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"></a>
  <a href="mailto:test@gmail.com"><img src="https://img.shields.io/badge/Email-Contact-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
</p>

---

## About Me 👋

Hi, thanks for stopping by! I'm a senior data scientist working at the intersection of **machine learning, messy healthcare data, and translational AI**. My work at **Massachusetts General Hospital** with building on prior applied ML role at the Broad Institute, **NIH via ASRT Inc.**, and **Bristol Myers Squibb** -> spans **predictive modeling, clinical NLP, explainable AI, developing foundation models, knowledge graphs and large-scale data pipelines** that turn fragmented clinical, EHR, biomedical, and multi-omic data into reliable, interpretable insight.

I care about healthcare ML that works **outside notebooks**: robust data pipelines, auditable model decisions, leakage-safe evaluation, clear explanations, and software that scales from local prototypes to large clinical datasets ->> *rigorous, reproducible, equitable across diverse populations, and explainable enough for domain experts to trust.*

🔭 **Currently focused on:** healthcare data-quality systems, entity resolution, clinical NLP, explainable predictive modeling, multimodal foundation models, and scalable ML pipelines.

---
## Current Projects &amp; healthcare AI Work 🚀

- **AI for Alzheimer's : OpenAI Foundation initiative.** Data Science Lead (MGH) within the [OpenAI Foundation's *AI for Alzheimer's*](https://openaifoundation.org/news/ai-for-alzheimers) initiative, a $100M+ program across six institutions for supporting the Mass General Brigham collaboration with the Institute for Protein Design (University of Washington). I build scalable, production-grade ML pipelines and active-learning loops that reason jointly across patient phenotypes, molecular biomarkers, and high-throughput screens to surface mechanistically interpretable, causally grounded drug targets, not black-box predictions.

- **RxFM ( Microsoft ) : Multimodal Foundation Model for ALS Therapeutic Science.** Building **RxFM** at MGH (home development site) on Microsoft's Discovery agentic-AI platform (Azure) which is a multimodal therapeutic foundation model that integrates multi-omic, single-cell, metabolomic, clinical, and drug-perturbation data into a unified framework for ALS drug discovery and repurposing. By framing the disease's heterogeneous pathophysiology as a network-perturbation problem, the model is designed to identify interventions that reverse complex disease signatures, and to be fine-tuned for zero-shot discovery in diseases with little known biology.

- **DRIAD-FL ( US, UK, Israel ) : Federated Learning across fragmented healthcare data.** Contributing data-science and **federated-learning** methods development for a **six-site, cross-country effort (UK, US, and Israel / Clalit)** -> building privacy-preserving FL methods for target-trial emulation, scaling across **100M+ healthcare records**, and developing reusable pipelines for learning across fragmented, multi-source healthcare data without centralizing it.
  > *Directly relevant to healthcare data quality at scale: privacy-preserving learning, cross-site harmonization, and reusable pipelines over high-volume, multi-source records.*

- Interpretable Multi-modal Patient Stratification ( **Google DeepMind collab** ) : Built an interpretable, multimodal deep-learning pipeline that fuses high-dimensional omics, rare pathogenic variants, and longitudinal clinical features to resolve a clinically heterogeneous population into molecularly defined subgroups. A variational autoencoder compresses these noisy signals into a shared latent space; explainability methods (SHAP, latent-space traversal) tie each latent dimension to pathway dysregulation and to outcomes such as functional decline and survival surfacing distinct molecular subtypes (oxidative/proteotoxic stress, TDP-43/transposable-element, and neuroinflammatory). The fused model improved subgroup separation and outcome prediction over single-omic baselines (94.1% AUROC vs. single modality-only), yielding transparent, reproducible strata for clinical decision support and trial enrichment. Built in Python (PyTorch, scikit-learn) as a modular, production-style pipeline over large clinical-omics cohorts (Northeast US, MGB and MA, NYGC, others..), with mentorship and resources from members of the **Google DeepMind** team (Zurich &amp; London).

---

## What I Build 🧩

I build ML systems for high-noise, high-stakes healthcare data:

| Healthcare ML problem | What I work on |
|---|---|
| **Messy healthcare records** | Data profiling, validation, schema-drift detection, missingness handling, normalization, and quality scoring |
| **Entity resolution** | Deduplication and cross-source linkage for patient / provider / member / drug master data |
| **Clinical NLP &amp; text mining** | Entity extraction, ontology normalization, summarization, search, and weak-supervision workflows |
| **Predictive modeling** | Risk, outcome, disease-progression, anomaly, and data-quality models with leakage-safe validation |
| **Explainable AI** | InterpretML, SHAP / LIME / coefficient-level explanations, interpretable features, audit trails, and model cards |
| **Scalable pipelines** | Python, R, Scala/Spark, PySpark, SQL, Docker, cloud/HPC workflows, and production-minded ML engineering |

---

## Featured Projects 🔬

### [DrugMesh](https://github.com/rbr7/DrugMesh) : Scala/Spark Entity Resolution for Biomedical Master Data

**A Spark-scale, explainable data-quality &amp; entity-resolution engine that reconciles drug records across 10+ public biomedical databases.**

DrugMesh ingests messy public drug sources, resolves which records refer to the *same* real-world entity despite missing identifiers and naming variation, flags inconsistent/bad records with confidence scores, and emits an auditable reason for every decision.

> **Why it matters:** this is the same master-data problem as cleaning provider directories, payer rosters, formulary and member records, and clinical reference tables.

- Scala + Apache Spark pipelines (typed `Dataset` DAG, broadcast joins, Adaptive Query Execution) for distributed entity resolution
- Probabilistic matching (blocking → string-similarity features → a **Fellegi-Sunter** matcher whose per-field log-odds *are* the explanation) plus an MLlib **GBT** trained on **Snorkel** weak-supervision labels
- Distributed **anomaly detection** (Isolation Forest over data-quality signals), **biomedical NER** (Spark NLP), BioBERT embeddings, and **Elasticsearch** search
- Explainable match scoring with per-field evidence + **SHAP/LIME**, with MUnit/ScalaCheck tests and a GitHub Actions CI matrix (Spark 3.5 &amp; 4.0)
- *A Scala/Spark re-implementation and extension of an open-source drug-mapping toolkit (attributed in the repo).*

`Scala` · `Apache Spark` · `Entity Resolution` · `Data Quality` · `Biomedical NLP` · `Elasticsearch` · `Explainability`

---

### [ClinClaw](https://github.com/rbr7/ClinClaw) : Healthcare Data Quality + Explainable Predictive Modeling

**A medical-AI harness for healthcare data quality, clinical NLP, and interpretable ML workflows.**

ClinClaw wraps ML/LLM components in a reusable execution harness (validation checkpoints, structured context, result validation, rollback, failure recovery). Its data-quality toolkit is built for records that are incomplete, inconsistent, duplicated, or text-heavy.

- Record profiling across **completeness, validity (NPI Luhn, ICD-10, ICD-10-CM, OMOP, ZIP, date, state), uniqueness, and consistency**, with record-level quality scoring and remediation recommendations
- Multivariate **anomaly detection** (IQR + scikit-learn Isolation Forest)
- **Clinical entity extraction** with synonym→canonical **ontology normalization** (spaCy/scispaCy)
- **Interpretable** from-scratch L2-regularized logistic regression (coefficients = feature importances; reports AUC/F1/precision/recall)
- **A/B testing** utilities and a **PySpark** data-quality pipeline (`load → standardize → dedup → validity/anomaly flags → write`) for record-scale claims data, with a runnable offline demo

`Python` · `PySpark` · `scikit-learn` · `Clinical NLP` · `Anomaly Detection` · `A/B Testing` · `Explainable ML`

---

### [MedClawMini](https://github.com/rbr7/MedClawMini) : Healthcare Data-Science Skill Library

**A curated library of clinical-AI and healthcare data-science workflows** spanning data quality, NLP, scalable ML, explainability, drug safety, and governance — codified as auditable, reusable skill modules.

Highlighted workflows: healthcare data-quality profiling · patient/provider/member entity resolution · claims anomaly detection · ICD/CPT/SNOMED/RxNorm/LOINC/UMLS mapping · clinical NER &amp; summarization · ELK/OpenSearch clinical search · Snorkel weak supervision · Spark/Scala healthcare ETL · explainable ML &amp; subgroup audits · A/B testing &amp; model validation.

`Healthcare Data Quality` · `Clinical NLP` · `Snorkel` · `Spark/Scala` · `ELK/OpenSearch` · `XAI` · `Model Governance`

---

### [MedSift](https://github.com/rbr7/MedSift) : Local Healthcare ML Workbench

**A privacy-first healthcare-ML workbench** that structures health records, then runs data-science workflows over them: clinical NER and concept tagging, data-quality normalization, statistical + Isolation-Forest anomaly detection, SHAP-style explanations, weak-supervision labeling, BM25 + dense hybrid search, and experiment evaluation (calibration, A/B, significance tests).

`Python` · `Clinical NLP` · `Data Quality` · `Anomaly Detection` · `SHAP` · `Weak Supervision` · `Hybrid Search`

---

### More on GitHub

| Project | What it does | Focus |
|---|---|---|
| [**PB-Dataset-Recommender_Engine**](https://github.com/rbr7/PB-Dataset-Recommender_Engine) | Biomedical-NLP recommender that searches &amp; ranks datasets across NCBI, SRA &amp; EBI | Bio-NLP · search/ranking |
| [**Human Protein Atlas : Kaggle 2021**](https://github.com/rbr7/Human_Protein_Atlas_challenge-kaggle-2021) | Weakly-supervised, multi-label classification of single-cell protein localization | weak supervision · multi-label DL |
| [**scRNASeq Workflow + Cell Predictions**](https://github.com/rbr7/scRNASeq-Workflow-and-Cell-predictions) | Single-cell RNA-seq analysis on the **Geneformer** transformer foundation model | transformers · embeddings |
| [**scMultiOmics Integration Tool**](https://github.com/rbr7/scMultiOmics-IntegrationTool) | Reproducible pipeline integrating single-cell ATAC-seq + RNA-seq | multi-omics · pipeline engineering |
| [**corral**](https://github.com/rbr7/corral) | Terminal dashboard that corrals tmux sessions &amp; Slurm jobs across SSH/compute nodes | software engineering · MLOps/HPC |
| [**RxFM**](https://github.com/rbr7/) |  | Foundation model · MLOps/HPC |
| [**CLIO**](https://github.com/rbr7/) |  | Clinical AI model · Clinical AI/HPC/Healthcare |
| [**PRISM**](https://github.com/rbr7/) |  | HGT model · LLMs/HPC |


## Experience 💼

- **Massachusetts General Hospital** : *Senior Data Scientist* · Boston, MA
- **Broad Institute** : *Data Scientist II* · Cambridge, MA
- **NIMHD (NIH) via ASRT Inc.** : *Bioinformatics Scientist* · Atlanta, GA
- **Bristol Myers Squibb** : *Applied ML Intern (Applied Bioinformatics)* · on-site
- **Georgia Tech : Computational Genomics Lab** -> *Graduate Research Assistant* · Atlanta, GA
- **GATK Team, Broad** : *Open-Source Developer* · remote
- **Quadrical.ai** : *Software Developer &amp; Data Scientist* · Gurugram, India
- **Elucidata** : *Data Science &amp; Analytics* · New Delhi, India

---

## Technical Toolbox 🧰

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![R](https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white)
![Scala](https://img.shields.io/badge/Scala-DC322F?style=for-the-badge&logo=scala&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=for-the-badge&logo=gnubash&logoColor=white)

**Machine Learning &amp; Deep Learning**

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-189AB4?style=for-the-badge)
![Hugging Face](https://img.shields.io/badge/Transformers%20·%20VAEs-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)

**NLP &amp; Text Mining**

![spaCy](https://img.shields.io/badge/spaCy%20·%20scispaCy-09A3D5?style=for-the-badge&logo=spacy&logoColor=white)
![Snorkel](https://img.shields.io/badge/Snorkel%20·%20Weak%20Supervision-1A1A1A?style=for-the-badge)
![Elasticsearch](https://img.shields.io/badge/Elasticsearch%20(ELK)-005571?style=for-the-badge&logo=elasticsearch&logoColor=white)

**Explainable AI**

![SHAP](https://img.shields.io/badge/SHAP-FF4B4B?style=for-the-badge)
![Captum](https://img.shields.io/badge/Captum-EE4C2C?style=for-the-badge)
![LIME](https://img.shields.io/badge/LIME-3CB371?style=for-the-badge)

**Big Data, Pipelines &amp; MLOps**

![Apache Spark](https://img.shields.io/badge/Apache%20Spark-E25A1C?style=for-the-badge&logo=apachespark&logoColor=white)
![Hadoop](https://img.shields.io/badge/Hadoop-66CCFF?style=for-the-badge&logo=apachehadoop&logoColor=black)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white)
![GCP](https://img.shields.io/badge/GCP-4285F4?style=for-the-badge&logo=googlecloud&logoColor=white)
![Nextflow](https://img.shields.io/badge/Nextflow%20·%20WDL-0DC09D?style=for-the-badge&logo=nextflow&logoColor=white)
![Git](https://img.shields.io/badge/Git%20·%20CI%2FCD-F05032?style=for-the-badge&logo=git&logoColor=white)

**Data Systems:** PostgreSQL · MongoDB · BigQuery · ETL · schema design · data validation
**Biomedical Data &amp; Cohorts:** EHR-linked cohorts · Kaiser Permanente, RPDR, CPRD, Clalit · UK Biobank · *All of Us* · MGB Biobank · CELLxGENE · GTEx · gnomAD · ClinVar · TCGA

---

## Service & Community 🤝

- **Reviewer**, Machine Learning for Health (**ML4H**) and Conference on Health, Inference, and Learning (**CHIL**)
- **Poster presentations** at ML4H and CHIL on [CLIO - Continuous-time clinical LLM-Informed Ordinal imputation, 2025; PRISM - Phenotype-Resolved Inference for Spectrum-wide Matching, 2026]

## Selected Publications 📄

A few representative papers with full list on [Google Scholar](https://scholar.google.com/citations?user=6RGIV64AAAAJ&hl=en).

---

## How I Work 🧭

I build systems where the model is only one part of the product. Good healthcare ML needs **clean, validated, documented data · explicit assumptions and leakage checks · reproducible experiments · interpretable outputs for clinical and business stakeholders · failure handling and monitoring · domain-expert feedback loops · and production-quality code a team can maintain.** That's the kind of healthcare AI I build.

---

<p align="center"><i>Open to conversations on healthcare data quality, explainable ML, clinical NLP, scalable ML systems, and foundation models for human health.</i></p>
