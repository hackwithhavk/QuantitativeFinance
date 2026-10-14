# SEC Financial Data Preprocessing

**Entry ID:** 2026-10-13-Sunji2468-sec-data-preprocessing  
**Title:** SEC Financial Data Processing  
**Author:** Sai Srujana Sri Vangapandu  
**Date Completed:** 2026-10-13

## 1. Objective

Download, clean, and combine SEC financial data files into a format that is faster and easier to use.

## 2. Background

The SEC financial statement dataset is over 100 GB in total. Raw text files require a large amount of memory and can be slow to load. Converting the data to Parquet reduces storage size and improves performance.

## 3. Dataset

- **Dataset:** SEC Financial Statement Data Sets
- **Coverage:** Q3 2026 filings (10-K and 10-Q)
- **Source:** https://www.sec.gov/data-research/sec-markets-data/financial-statement-data-sets

## 4. Conclusion

Reducing the number of columns before joining tables lowered memory usage. The resulting Parquet file is smaller, loads faster, and can be used for future analysis and AI model development.

## 5. Limitations

- Only one quarter of SEC data was tested.
- Historical SEC datasets have not been tested yet.

## 6. Next Steps

- Process SEC data from 2014–2026.
- Convert the notebook workflow into a Python script.
- Map SEC CIK values to stock ticker symbols.
