# Curated Voice: Communicative Inequality and Platform Power in NFT and DeFi Communities on X

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://github.com/Joceelin/Curated-Voice-Data/blob/main/LICENSE)
[![Data: X (Twitter)](https://img.shields.io/badge/Platform-X%20(Twitter)-black)](https://x.com)
[![Period: 2025](https://img.shields.io/badge/Period-January–December%202025-blue)]()

---

## 📄 About This Repository

This repository contains the dataset used in the paper:

> **"Curated Voice: Communicative Inequality and Platform Power in NFT and DeFi Communities on X"**
> *(Submitted to New Media & Society)*

The dataset supports analysis of communicative inequality and platform power dynamics within NFT (Non-Fungible Token) and DeFi (Decentralized Finance) communities on X (formerly Twitter). The repository is shared to ensure transparency and reproducibility in accordance with the journal's data availability policy.

---

## ⚠️ Data Availability Statement

The data supporting the findings of this study were obtained from X (formerly Twitter) through a third-party data provider and **cannot be publicly shared in raw form** due to platform Terms of Service restrictions.

The dataset provided in this repository has been processed to comply with platform policies and ethical standards. Specifically, only the tweet text (`full_text`) is retained, while usernames have been **anonymized through hashing** to protect user identities. All other metadata has been removed. The data collection procedure, sampling strategy, preprocessing steps, and analytical parameters are described in detail in the **Methods section** and **Supplementary Material** of the paper.

---

## 📁 Repository Structure

```
Curated-Voice-Data/
│
├── data/
│   ├── NFT_Communities_Dataset.csv    ← NFT community tweets
│   └── DeFi_Communities_Dataset.csv  ← DeFi community tweets
│
└── README.md
```

---

## 📊 Dataset Description

**Collection period:** January – December 2025  
**Platform:** X (formerly Twitter)  
**Communities:** NFT and DeFi discourse (two separate files)

| File | Community | Description |
|---|---|---|
| `NFT_Communities_Dataset.csv` | NFT | Tweets from NFT-related communities and discourse |
| `DeFi_Communities_Dataset.csv` | DeFi | Tweets from DeFi-related communities and discourse |

### Column Dictionary

| Column | Description |
|---|---|
| `username` | Anonymized account identifier (hashed to protect user identity; original usernames are not recoverable) |
| `full_text` | Full text content of the tweet |

> **Note on anonymization:** Usernames have been irreversibly hashed using a one-way hashing method prior to publication. This anonymization was applied to comply with X's Terms of Service and to protect the privacy of platform users.

---

## 🔍 Data Collection

- **Period:** January 2025 – December 2025
- **Method:** Collected via a third-party data provider using keyword and hashtag filtering relevant to NFT and DeFi discourse on X
- **Sampling strategy:** Described in detail in the Methods section of the paper
- **Preprocessing:** Described in the Supplementary Material of the paper

---

## ⚖️ License

The dataset in this repository is shared under [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://github.com/Joceelin/Curated-Voice-Data/blob/main/LICENSE).

You are free to share and adapt the material for any purpose, provided appropriate credit is given.

> **Note:** This dataset is derived from X (formerly Twitter). Users of this data are responsible for complying with [X's Terms of Service](https://x.com/en/tos) and applicable data protection regulations.

---

## 📬 Contact

For questions about the dataset, please open a [GitHub Issue](../../issues) or contact the corresponding author as listed in the manuscript.

---

## 🙏 Acknowledgements

Data collection was conducted using a third-party provider in accordance with X platform policies at the time of collection. The authors acknowledge that platform Terms of Service restrict the redistribution of raw tweet content.
