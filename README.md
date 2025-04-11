# Fund and Stock Sparsity Project

This research project investigates **portfolio sparsity** and **stock coverage** among mutual funds, exploring how these characteristics relate to fund performance, persistence, and asset pricing factors. The analysis is conducted using Python (Jupyter Notebooks) and Stata, and covers a broad empirical pipeline from data cleaning to regression analysis.

## Project Structure

### 1. Fund Sparsity Construction
**`01_fund_sparisty.ipynb`**  
- Constructs fund-level sparsity measures.
- Computes `Percent Within Fund` and `Percent Benchmark` across multiple horizons (e.g., 3, 7, 11, 15, 19 quarters).
- Benchmarks are updated to reflect dynamic fund universes.

### 2. Benchmark Updating
**`02_Updating_Benchmark_Fund_Sparisty.ipynb`**  
- Refines benchmark universes for better comparison across funds.
- Ensures accurate matching between fund holdings and benchmark constituents over time.

### 3. Exploratory Data Analysis (EDA)
**`03_fund_sparsity_EDA.ipynb`**  
- Provides descriptive statistics and visualizations of fund sparsity.
- Examines variation across time and fund types.

### 4. Persistency and Performance
**`04_fund_sparisty_persistency_performance.log`**  
- Runs fixed-effects panel regressions in Stata.
- Tests persistence of sparsity metrics and their predictive power on fund returns under various model specifications:
  - Fund & time fixed effects
  - Market and FF3 interactions

### 5. Fund-Level Cross-Sectional Analysis
**`05_fund_cross_sectional_analysis.ipynb`**  
- Analyzes the cross-sectional relationship between fund sparsity and characteristics like size, turnover, and performance.

### 6. Stock-Level Sparsity and Coverage
**`06_stock_sparisty_coverage_ratio_constructions.ipynb`**  
- Constructs stock-level sparsity and mutual fund coverage ratios.

### 7. Linking Stock Characteristics to Returns
**`07_Merge_stock_sparsity with Average Daily Returns and Alpha.ipynb`**  
- Merges stock sparsity proxies with realized returns and alpha estimates.

### 8. Decile Portfolio Regressions
**`08_deciles_return_regression.ipynb`**  
- Sorts stocks into deciles based on sparsity.
- Runs Fama-French-style regressions to assess return patterns.

### 9. Hard-to-Value Proxy Correlation
**`09_Hard_to_Value_proxy_Correlation_Matrix.ipynb`**  
- Correlation analysis between sparsity and “hard-to-value” proxies such as:
  - Analyst coverage
  - Return volatility
  - Valuation spreads

### 10. Investor Concentration Measures
**`10_investor_concentration_proxy_constructions.ipynb`**  
- Builds fund concentration and ownership dispersion metrics to complement sparsity measures.

---

## Usage

- **Dependencies**: Python 3.x, pandas, numpy, matplotlib, seaborn, statsmodels, and Stata for the `.log` regressions.
- **Data Inputs**: Mutual fund holdings data, CRSP/Compustat, benchmark index compositions.
- **Execution Order**: Run notebooks in numeric order (`01_` to `10_`) for full pipeline reproducibility.

## Author

Zi Wang, with support from research collaborators.

## License

Proprietary – for academic research use only.
