# Curated Voice: Communicative Inequality and Platform Power in NFT and DeFi Communities on X

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](LICENSE)
[![Data: X (Twitter)](https://img.shields.io/badge/Platform-X%20(Twitter)-black)](https://x.com)
[![Period: 2025](https://img.shields.io/badge/Period-January–December%202025-blue)]()

---

## 📄 About This Repository

This repository contains the official dataset and Python implementation code used in the research manuscript:

> **"Curated Voice: Communicative Inequality and Platform Power in NFT and DeFi Communities on X"**
> *(Submitted to New Media & Society)*

The repository is shared to ensure transparency, reproducibility, and verification of our findings in accordance with the journal's data availability policy. By combining **Social Network Analysis (SNA)** and **Information Theory (Shannon Entropy & Jensen-Shannon Divergence)**, the provided pipeline evaluates how structural prominence within token networks shapes online public discourse.

---

## ✒️ Citation

If you use this dataset, the replication code, or the methodological framework in your research, please cite it as specified in the [CITATION.cff](CITATION.cff) file or using the following format:

> Juono, W. J., Ramadhani, D. P., & Alamsyah, A. (2026). *Code and annotated data for "Curated Voice: Communicative Inequality and Platform Power in NFT and DeFi Communities on X"*. GitHub Repository. Available at: https://github.com/Joceelin/Curated-Voice-Data

---

## ⚠️ Data Availability Statement

The data supporting the findings of this study were obtained from X (formerly Twitter) through a third-party data provider and **cannot be publicly shared in raw form** due to platform Terms of Service restrictions.

The dataset provided in this repository has been processed to comply with platform policies and ethical standards. Specifically, only the tweet text (`full_text`) is retained, while usernames have been **anonymized through hashing** to protect user identities. 

---

## 📁 Repository Structure

```
Curated-Voice-Data/
│
├── data/
│   ├── NFT_Communities_Dataset.csv    ← NFT community tweets
│   └── DeFi_Communities_Dataset.csv   ← DeFi community tweets
│
├── CITATION.cff                       ← Citation metadata file
├── LICENSE                            ← Creative Commons Attribution 4.0 License
├── Shannon_Entropy_JSD.ipynb          ← Computational analysis pipeline
└── README.md                          ← This file
```

---

## 📊 Dataset Description

**Collection period:** January – December 2025  
**Platform:** X (formerly Twitter)  
**Communities:** NFT and DeFi discourse (two separate files)

| File | Community | Description |
|---|---|---|
| `data/NFT_Communities_Dataset.csv` | NFT | Tweets from NFT-related communities and discourse |
| `data/DeFi_Communities_Dataset.csv` | DeFi | Tweets from DeFi-related communities and discourse |

### Column Dictionary

| Column | Description |
|---|---|
| `username` | Anonymized account identifier (hashed to protect user identity; original usernames are not recoverable) |
| `full_text` | Full text content of the tweet |

> **Note on anonymization:** Usernames have been irreversibly hashed using a one-way hashing method prior to publication. This anonymization was applied to comply with X's Terms of Service and to protect the privacy of platform users.

---

## ⚙️ Analytical Framework & Pipeline Settings

The accompanying Jupyter Notebook (`Shannon_Entropy_JSD.ipynb`) implements a multi-stage computational pipeline:

### 1. Actor Classification (Top-3 Empirical Break-Point Threshold)
Instead of relying on arbitrary statistical percentiles, this pipeline segregates the communication layers into **Central-Actor-Associated Discourse** and **Regular Actor Discourse** using an empirical structural break-point threshold. Central actors are defined strictly as the **top 3 accounts** ranked by **Total Weighted Degree** (combined incoming and outgoing interaction weights). 

### 2. Domain-Specific Text Preprocessing
To prevent pervasive background terminology from dominating frequency distributions and obscuring thematic variations, the clean-up script filters out standard English stop words along with specific domain-level keywords: `crypto`, `blockchain`, `web3`, `defi`, `nft`, `opensea`, `ethereum`, `eth`, `btc`, and `bitcoin`.

### 3. Core Information-Theoretic Metrics
* **Gini Coefficient:** Evaluates the degree of interaction inequality and structural concentration across the network.
* **Shannon Entropy ($H$):** Measures the internal unigram lexical diversity within each actor group to detect thematic concentration.
* **Jensen-Shannon Divergence (JSD):** Computes the mathematical distance between elite framing and community discourse over a shared top-1000 term vocabulary space, bounded strictly between `0.0` (identical distributions) and `1.0` (completely divergent).

---

## 🚀 Execution & Replication Steps

To replicate the text-based discourse diversity analysis using [Google Colab](https://colab.research.google.com/):

1. **Upload Notebook:** Download `Shannon_Entropy_JSD.ipynb` from this repository and upload it into your Google Colab workspace.
2. **Data Input Requirements:** When prompted by the execution script, upload your target communication and interaction files:
   * **Tweet Data CSV:** Must contain a user handle column (`username`) and the raw text body (`full_text`).
   * **Edgelist CSV:** Must map network structural ties using `source`, `target`, and `weight` columns.
3. **Run Pipeline:** Execute the code cells sequentially. The script will automatically parse the network topology, extract the top 3 central actors, clean the textual records, and output the Lorenz curves, Shannon Entropy bars, and JSD gauge visualization.

---

## 🔍 Data Collection

- **Period:** January 2025 – December 2025
- **Method:** Collected via a third-party data provider using keyword and hashtag filtering relevant to NFT and DeFi discourse on X
- **Sampling strategy:** Described in detail in the Methods section of the paper
- **Preprocessing:** Described in the Supplementary Material of the paper

---

## ⚖️ License

The dataset and code in this repository are shared under [Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE).

You are free to share and adapt the material for any purpose, provided appropriate credit is given.

> **Note:** This dataset is derived from X (formerly Twitter). Users of this data are responsible for complying with [X's Terms of Service](https://x.com/en/tos) and applicable data protection regulations.

---

## 📬 Contact

For questions about the dataset or code implementation, please open a [GitHub Issue](../../issues) or contact the corresponding author as listed in the manuscript.

---

## 🙏 Acknowledgements

Data collection was conducted using a third-party provider in accordance with X platform policies at the time of collection. The authors acknowledge that platform Terms of Service restrict the redistribution of raw tweet content.
README.md
Displaying README.md.
