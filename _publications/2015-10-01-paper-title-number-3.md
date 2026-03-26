---
title: "The Propagation Path of Jump Risk in the Stock Market"
collection: publications
permalink: /publication/2023-jump-risk-propagation
excerpt: 'This paper identifies the propagation paths of jump risk in the stock market by combining high-frequency data with network analysis. The results reveal six risk communities and key transmission channels, showing that the securities community is the main source of jump risk, which spreads to the broader market and then to energy and infrastructure sectors.'
date: 2023-06-30
venue: 'Working paper'
paperurl: ''
citation: 'He, Sixuan, and Cheng Liu. (2023). &quot;The Propagation Path of Jump Risk in the Stock Market.&quot; Working paper.'
status: 'Under review'
---

## Abstract

This paper investigates the propagation paths of jump risk in China’s stock market using high-frequency data from 196 CSI 300 constituents over 2013–2022. We employ nonparametric threshold methods to identify stock jumps and cojumps, and apply the Spectral Clustering on Ratios-of-Eigenvectors (SCORE) algorithm to detect communities within the stock cojump network. Six distinct risk communities are identified: Energy, Military, Infrastructure, Securities, “Ballast” (large-cap blue chips including banks, insurers, and real estate), and Broad Market. By constructing daily jump intensity measures for each community and applying Directed Acyclic Graph (DAG) analysis, we uncover contemporaneous causal relationships among communities. Our results show that the Securities community is the primary source of jump risk transmission, followed by the Military community. Jump risk propagates from Securities to the Broad Market and Ballast communities, and further to Energy and Infrastructure communities. The Broad Market also transmits risk to the Ballast community, reflecting a diffusion from short-term to long-term investors. These findings provide insights for risk monitoring and policy anticipation management.

**Keywords:** Information shock; Jump risk; Price cojump; Community detection; Directed acyclic graph

## Methods Overview

- **Jump and cojump identification:** Nonparametric threshold estimator (Mancini, 2009) using 5‑minute high‑frequency data.
- **Community detection:** Spectral Clustering on Ratios-of-Eigenvectors (SCORE; Jin, 2015) applied to the stock cojump network, with the number of communities selected by maximizing a criterion that balances community homogeneity and industry interpretability.
- **Risk transmission analysis:** Daily community jump intensity is defined and contemporaneous causal relationships are recovered via the PC algorithm for Directed Acyclic Graphs (DAG) on the innovation correlation matrix of a VAR(0) model.

## Key Findings

- Six communities with distinct risk profiles are identified: Energy, Military, Infrastructure, Securities, Ballast, and Broad Market.
- The Securities community is the most frequent source of extreme jump risk and acts as the primary transmitter to the Broad Market and Ballast communities.
- Risk propagates from the Broad Market to the Ballast community, indicating a diffusion from short‑term to long‑term investors.
- The Energy and Infrastructure communities are net receivers of jump risk, mainly driven by shocks from the Broad Market and Ballast communities.
- The Military community exhibits a relatively independent risk structure but still transmits risk to the Broad Market.

The paper is currently under review. A full draft is available upon request.

## Recommended citation

He, Sixuan, and Cheng Liu. (2023). "The Propagation Path of Jump Risk in the Stock Market." Working paper.