# Medical Coding & Pharmacovigilance (PV) Data Annotation Project
### Technology Stack: Doccano, Oracle Argus Safety Workflow Framework, MedDRA Staging

## 📋 Project Overview
This project simulates an advanced clinical data pipeline translating raw, unstructured oncology trial reports and adverse event narratives into machine-readable datasets. Utilizing **Doccano**, I built a structured sequence labeling framework to isolate critical medical terms. 

This directly replicates the foundational preprocessing steps required to automate global **MedDRA medical coding** and streamline clinical case processing workflows commonly executed within safety databases like **Oracle Argus Safety**.

---

## 🏷️ Advanced Pharmacovigilance Taxonomy Applied
The text corpora were annotated using standard industry definitions:
* **`MEDDRA_INDICATION`**: Primary oncological conditions, staging criteria, and malignant classifications requiring therapeutic intervention.
* **`MEDDRA_SUSPECT_ADVERSE_EVENT`**: Toxicities, lab abnormalities, and unexpected patient events suspected of being treatment-related.
* **`SUSPECT_DRUG`**: Primary oncology therapies, immunotherapies, and clinical investigational agents under safety monitoring.
* **`CONCOMITANT_DRUG`**: Concurrently administered treatments, including baseline prophylactic antiemetics, corticosteroids, and supportive therapies.

---

## 💻 Tech Stack & Tools
* **Annotation Environment:** Doccano (Sequence Labeling Project Type)
* **Source Format:** JSON Lines (`.jsonl`)
* **Version Control:** GitHub

---

## 🚀 Workflow Execution

### 1. Project Configuration
* Initialized a **Sequence Labeling** instance within Doccano.
* Configured a distinct, color-coded palette for clinical labels to ensure high visual contrast and accuracy during labeling passes.

### 2. Annotation Guidelines Applied
* **Strict Boundary Selection:** Only the direct clinical terms are highlighted (e.g., capturing the precise drug name without surrounding prepositions).
* **Overlapping Entities:** Prioritized nested biomarkers within complex diagnostic phrasing according to standard NLP preprocessing practices.

### 3. Export & Delivery
* Extracted the annotated text blocks back into a structured `.jsonl` schema matching standard Hugging Face/NLP training payload layouts.

---

## 📁 Repository Structure
* `meddra_argus_oncology_50_samples.jsonl`: The raw text database populated with unstructured trial descriptions.
* `README.md`: Project summary, setup rules, and portfolio presentation details.

# Medical-coding-pharmacovigilance-Annotation
An Oncology clinical trial data annotation project  mapping unstructured patient narratives to MeDRA medical coding  and pharmacovigilance work flow using Doccano.
