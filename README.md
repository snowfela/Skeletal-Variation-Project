# 🦴 Skeletal Variation

## Overview
This project explores **skeletal variation across humans, mammals, and birds**, revealing fascinating insights into **evolutionary biology** and the **structural diversity** of vertebrate anatomy. The analysis focuses on bone-count distributions, fusion patterns, and neck bone comparisons to understand evolutionary consistency and adaptations among species.

## Objectives
- Analyze the **adult human skeleton** dataset (`adult-human-skeleton.csv`) to understand bone distribution.  
- Investigate the **proportion of bones in the hands and feet** to verify the claim that over half of human bones are located there.  
- Study **bone fusion patterns** in infants and adults to calculate total bone counts at different developmental stages.  
- Compare **neck bone structures** in humans, mammals, and birds to uncover variations and evolutionary similarities.

## Dataset
The project uses three main datasets:
- `adult-human-skeleton.csv` — Contains information about every bone in the adult human body.  
- `mammal-neck-bones.csv` — Lists neck bones in various mammals.  
- `bird-neck-bones.csv` — Lists neck bones in different bird species.

Each dataset includes anatomical names, regions, and fusion data for comparative analysis.

## Key Steps and Analysis

### 1. Data Loading and Exploration
- Loaded datasets using `pandas` for tabular analysis.
- Displayed the human skeletal dataset to verify completeness (206 bones total).

### 2. Verifying the “Half the Bones” Claim
- Counted the number of bones in each region using `value_counts()`.
- Found that:
  - Hands: 54 bones  
  - Feet: 52 bones  
  - Together: 106 bones  
- Calculation → `(54 + 52) / 206 ≈ 0.514`  
  ✅ **Claim confirmed:** Over 51% of human bones are in the hands and feet.

### 3. Analyzing Bone Fusion
- Investigated the `fused_from` column to identify fused bones.
- Sorted bones by fusion count to find regions with high fusion (e.g., sternum = 6 fused bones).
- Summed all fusions: `305` bones in infants → `206` bones in adults due to natural fusion during growth.

### 4. Neck Bone Comparisons
- Queried the human dataset for neck bones (`region == 'neck'`).
- Found **7 cervical vertebrae (C1–C7)** plus one throat bone.
- Compared this with mammal and bird datasets:
  - Mammals typically also have **7 neck vertebrae**, regardless of neck length (e.g., giraffes).
  - Birds show **greater variation**, with some species having up to **25 neck vertebrae**, allowing for increased flexibility and mobility.

## Tools & Libraries
- **Python**  
- **Pandas** for data manipulation and analysis
- **Matplotlib** for data visualization  
- **Google Colab** for execution and file uploads  

## Key Insights
- Over half of the bones in the human body are in the hands and feet.  
- Infants have ~305 bones; many fuse into 206 bones by adulthood.  
- Most mammals share the same number of neck vertebrae (7), a strong evolutionary constraint.  
- Birds display remarkable skeletal flexibility with widely varying neck bone counts.

## Author
Created as an analytical exercise in **comparative anatomy** and **data-driven evolutionary biology** using Python and open datasets.
