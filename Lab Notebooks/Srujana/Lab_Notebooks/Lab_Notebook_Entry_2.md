# SEC Data Exploratory Data Analysis & Visualization

**Entry ID:** 2026-10-21-Sunji2468-sec-data-vis  
**Title:** SEC Data EDA & Visualization  
**Author:** Sai Srujana Sri Vangapandu  
**Date Completed:** 2026-10-21

## 1. Objective

Check that the cleaned SEC Parquet dataset is correct by creating charts for important financial values.

## 2. Background

Before moving the cleaned dataset to the Jetson Orin Nanos for PyTorch time-series modeling, we need to make sure the financial data was extracted correctly. Since company sizes and wealth vary a lot, we used methods like removing duplicates and using log-scale charts to better spot unusual values or possible extraction mistakes.

## 3. Dataset

- **Dataset:** `2026_q3_financials_clean.parquet` (Generated pipeline output)
- **Coverage:** Q3 2026 filings (10-K and 10-Q)
- **Source:** Local processed output from https://www.sec.gov/data-research/sec-markets-data/financial-statement-data-sets

## 4. Conclusion

The charts showed that the data pipeline worked correctly. Count plots, bar charts, and log-scale histograms helped verify that financial values matched the correct companies. The log-scale visualizations also showed the expected distribution of company cash balances, with no major errors or unusual patterns.

## 5. Limitations

- Using only specific accounting tags, such as "Assets", may miss companies that use custom SEC taxonomy labels.
- The analysis only covers one quarter and does not show trends over time.

## 6. Next Steps
- Match SEC CIK numbers with stock ticker symbols using the SEC JSON mapping file.
- Process historical SEC data from 2014 to 2026 and store it directly on the Jetson NVMe drive.
- Build traditional Discounted Cash Flow (DCF) calculations to use as a baseline for comparison with machine learning models.
