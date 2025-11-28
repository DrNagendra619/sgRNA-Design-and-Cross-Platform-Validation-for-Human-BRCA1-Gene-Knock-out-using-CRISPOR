# sgRNA-Design-and-Cross-Platform-Validation-for-Human-BRCA1-Gene-Knock-out-using-CRISPOR
Comprehensive sgRNA Design and Cross-Platform Validation for Human BRCA1 Gene Knock-out using CRISPOR
# Comprehensive sgRNA Design and Cross-Platform Validation for Human BRCA1 Gene Knock-out using CRISPOR

### 🧬 Project Overview

This repository documents the target site selection process for a CRISPR/Cas9-mediated **gene knock-out** targeting the human **BReast CAncer gene 1 (BRCA1)**. The analysis was conducted using the **CRISPOR** design tool (targeting *Homo sapiens*, genome assembly GRCh38).

***

### 🔬 Genomic Context (Cross-Platform Analysis)

The sgRNA targets were validated against two major gene annotation systems to confirm their precise location within the critical coding region on **Chromosome 17**.

| System | Gene Model | Target Exon | Genomic Location Detail |
| :--- | :--- | :--- | :--- |
| **UCSC Model** | uc002byh.4 | **Exon 10** | Confirmed target location on Chromosome 17. |
| **Ensembl Model**| ENST00000357654.8 | **Exon 10** | Targets confirmed across both models to ensure maximum transcript coverage. |


***

### 🎯 Key Findings: Optimal sgRNA Candidates

The sgRNAs were prioritized based on the **MIT Off-Target Score (Specificity)** and the **Doench Score (Efficiency)**, as shown in the combined summary.

| Rank (by MIT Score) | sgRNA Sequence (20 nt) | PAM | Location (Start) | Strand | MIT Score (Specificity) | Doench Score (Efficiency) |
| :---: | :--- | :--- | :--- | :---: | :---: | :---: |
| **1** | **GCAGAAGTGGTAAGTTTAAC** | **GGG** | 43,124,375 | + | **100** | 0.44 |
| **2** | **CTCTTGGATCTTCTCTTTCT** | **TGG** | 43,124,198 | - | **100** | 0.35 |
| **3** | **GGCCATTCTTCCTCGTCAAC** | **TGG** | 43,125,584 | + | 99.8 | **0.67** |

*Interpretation: Rank 1 and 2 offer **perfect specificity (MIT 100)**. Rank 3 is the **highest-efficiency** cutting guide (0.67).*

#### **Specificity (Off-Target Analysis for Rank 1/2)**

The top sgRNAs demonstrate extremely low off-target risk.

| Off-Target Mismatches (MM) | Count | Interpretation |
| :---: | :---: | :--- |
| **MM0 (Perfect Match)** | **0** | No off-target sites found (essential for experimental safety). |
| **MM1 (1 Mismatch)** | **0** | No highly similar off-target matches found. |
| **MM2 (2 Mismatches)** | **1** | Only one low-risk off-target found. |

#### **Predicted Knock-out Outcome (Repair Profile)**

The analysis of predicted repair outcomes strongly suggests a high probability of generating a functional knock-out via Non-Homologous End-Joining (NHEJ).

| Metric | Predicted Value | Interpretation |
| :--- | :--- | :--- |
| **Frameshift Frequency** | **44.91%** | The predicted probability of achieving a successful gene-inactivating frame-shift mutation. |
| **Amplicon Size for Sequencing** | **~367 bp** | Ideal length for routine Sanger sequencing confirmation. |
| **RFLP Compatibility** | Detectable using various restriction enzymes (e.g., HpyAV, DdeI, NlaIV). |

***

### 📂 File Structure

| File Name | Content |
| :--- | :--- |
| `BRCA 1 Gene CRISPOR.html` | The comprehensive summary table and combined off-target analysis for all sgRNA candidates. |
| `BRCA1 GENE CRISPOR ENSEMBL.html` | Visualization and sequence context validated against the Ensembl gene model. |
| `BRCA1 Gene CRISPOR UCSC Gene Mode.html` | Visualization and sequence context validated against the UCSC gene model. |
| `BRCA 1 Gene CRISPOR.pdf` | PDF version of the comprehensive summary table and analysis. |
| `BRCA1 GENE CRISPOR ENSEMBL.pdf` | PDF version of the Ensembl gene model visualization. |
| `BRCA1 Gene CRISPOR UCSC Gene Mode.pdf` | PDF version of the UCSC gene model visualization. |
