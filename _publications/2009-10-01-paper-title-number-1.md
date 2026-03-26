---
title: "High-dimensional Multivariate Realized Volatility Forecasting with Community Network Structure"
collection: publications
permalink: /publication/2026-02-18-high-dimensional-multivariate-realized-volatility-forecasting
excerpt: 'We introduce the Community Network Heterogeneous Autoregressive model with Quarticity (CNHARQ), which integrates network-based information to enhance multivariate realized volatility forecasting. A Correlation-Based Stochastic Block Model (CBSBM) uncovers latent community structures, reducing parameter dimensionality and improving out-of-sample forecast accuracy over static industry classifications.'
date: 2026-02-18
venue: 'Journal of Business & Economic Statistics (accepted author version)'
paperurl: 'https://doi.org/10.1080/07350015.2026.2632810'
mathjax: true
citation: 'He, Sixuan, and Cheng Liu. (2026). &quot;High-dimensional Multivariate Realized Volatility Forecasting with Community Network Structure.&quot; <i>Journal of Business & Economic Statistics</i>. (accepted author version, posted online February 18, 2026)'
---

## Abstract

We introduce the Community Network Heterogeneous Autoregressive model with Quarticity (CNHARQ), a novel framework that integrates network-based information to enhance the forecasting of multivariate realized volatilities. To address the curse of dimensionality, we propose a Correlation-Based Stochastic Block Model (CBSBM) to uncover latent community structures from the correlation network of realized volatilities of \(N\) assets. This approach reduces the number of unknown parameters in the model from \(O(N^2)\) to \(O(NK)\), where \(K \ll N\) denotes the number of communities. Empirical analysis demonstrates that the CBSBM captures dynamic community structures, revealing shifts in the co-movement of asset volatilities over time. Furthermore, the CBSBM-based community structure outperforms the conventional Global Industry Classification Standard (GICS) in out-of-sample volatility forecasting, highlighting the superior forecasting power of network-based correlations over traditional industry classification schemes.

**Keywords:** Financial Network; High-frequency data; Community detection; High-dimensional data; HARQ.

---

## Methods Overview

The proposed **CNHARQ** model extends the univariate HARQ framework to a multivariate setting by incorporating network spillovers:

$$
\begin{aligned}
\mathbf{RV}_t = &\; \mathbf{I}_N\boldsymbol{\beta}_0 + \operatorname{diag}(\mathbf{RV}_{t-1})(\operatorname{diag}(\mathbf{RQ}_{t-1}^{1/2})\boldsymbol{\beta}_{1Q} + \boldsymbol{\beta}_1) \\
& + \operatorname{diag}(\mathbf{RV}_{t-1}^w)\boldsymbol{\beta}_2 + \operatorname{diag}(\mathbf{RV}_{t-1}^m)\boldsymbol{\beta}_3 + \mathbf{\Gamma}\boldsymbol{\theta}\mathbf{\Gamma}^\top \mathbf{RV}_{t-1} + \boldsymbol{\epsilon}_t,
\end{aligned}
$$

where $\mathbf{RV}_t$ is the vector of realized volatilities, $\mathbf{RQ}_t$ the realized quarticities, $\mathbf{\Gamma}$ the community membership matrix, and $\boldsymbol{\theta}$ the community-level network effect matrix.

The latent community structure $\mathbf{\Gamma}$ is estimated by the **Correlation-Based Stochastic Block Model (CBSBM)**:
- **Step 1:** Extract structural correlations $\mathbf{C}^{(s)}$ from the realized volatility correlation matrix using Random Matrix Theory (RMT).
- **Step 2:** Build the adjacency matrix $\mathbf{A}$ by thresholding $\mathbf{C}^{(s)}$ using a data-driven minimum-within-variance rule.
- **Step 3:** Apply spectral clustering to $\mathbf{A}$ to obtain $\mathbf{\Gamma}$, with the number of communities $K$ determined by eigenvalue thresholding.

---

## Data

We use tick-by-tick trading data of S&P 500 constituents from the TAQ database, covering January 1, 2013 to December 31, 2022 (2,518 trading days). After cleaning, 406 assets remain. Realized volatility is computed using 5‑minute and 10‑minute log-returns. The Global Industry Classification Standard (GICS) provides a static benchmark for comparison.

---

## Empirical Results

### Community Detection
CBSBM reveals time-varying community structures that are only partially aligned with GICS sectors. Utilities and Energy exhibit persistently high clustering levels, while sectors like Communication Services and Consumer Staples are more dispersed across communities. Major events such as the 2018 volatility spike and the 2022 energy shock induce structural shifts in community composition.

### In-Sample Fit
Both CNHAR and CNHARQ with CBSBM-based communities achieve higher \(R^2\) than HAR(Q) benchmarks. The network effects \(\hat{\boldsymbol{\theta}}\) show strong cross-community spillovers, with the Energy sector exerting a particularly strong influence on others.

### Out-of-Sample Forecast Performance
Using a 1000‑day rolling window, CNHARQ-CBSBM achieves the lowest root mean squared errors (RMSE) across all assets. The outperformance percentage (OP) relative to the HAR model is **99.26%** for the full forecast period, far exceeding that of HAR-GIRV (∼70–90%) and CNHARQ-GICS (∼20–40%). The gains are especially pronounced during the COVID-19 crisis in 2020, where the mean RMSE ratio drops to 0.063 (5‑minute) and the OP exceeds 99.5%. Results are robust to sampling frequency and window length.

---

## Conclusion

We develop the CNHARQ model that integrates data-driven community structures into multivariate realized volatility forecasting. The CBSBM identifies latent groups of assets with similar volatility correlation patterns, reducing dimensionality and capturing dynamic interdependencies. Out-of-sample results show that CBSBM-based communities consistently improve forecast accuracy over static GICS sectors, particularly during turbulent periods. This framework bridges network science and volatility forecasting, offering a flexible tool for high-dimensional financial time series.

---

## Data Availability

Deidentified data and replication code are available at:
[https://doi.org/10.6084/m9.figshare.29302937.v1](https://doi.org/10.6084/m9.figshare.29302937.v1)

---

## Recommended Citation

He, Sixuan, and Cheng Liu. (2026). "High-dimensional Multivariate Realized Volatility Forecasting with Community Network Structure." *Journal of Business & Economic Statistics*. (accepted author version, posted online February 18, 2026)

[Access the article online](https://doi.org/10.1080/07350015.2026.2632810)