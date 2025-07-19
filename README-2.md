# Dividend Portfolio Data Collection - README

## Project Overview

This project demonstrates a simple yet robust system for collecting, validating, and analyzing dividend-related data for a custom-designed stock portfolio. The solution is built using free APIs like `yfinance` and `Alpha Vantage`, and it follows industry-grade data validation practices suitable for beginner-to-intermediate financial analysts.

## Portfolio Design

The portfolio includes five diversified stocks across sectors:
- Apple Inc. (AAPL) – Technology
- Johnson & Johnson (JNJ) – Healthcare
- Coca-Cola (KO) – Consumer Staples
- PepsiCo (PEP) – Consumer Discretionary
- Emerson Electric (EMR) – Industrials

These securities were chosen based on their sector diversity, reliable dividend history, and representation of both growth and stability characteristics.

## Features

- Collects dividend and stock price data using the `yfinance` API.
- Validates selected stock data against Alpha Vantage for quality assurance.
- Screens stocks based on dividend yield and payout ratio thresholds.
- Implements error handling and missing data protection.
- Saves collected data to CSV for backup and reproducibility.

## Setup Instructions

1. Clone the repository:
   ```
   git clone https://github.com/yourusername/your-repo-name.git
   cd your-repo-name
   ```

2. Create a virtual environment (optional but recommended):
   ```
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

4. Add your Alpha Vantage API key in the script:
   ```python
   api_key = 'YOUR_ALPHA_VANTAGE_API_KEY'
   ```

5. Run the script:
   ```
   python main.py
   ```

## Files Included

- `main.py` – Main script with data collection, validation, and screening logic.
- `README.md` – This file.
- `requirements.txt` – Lists required Python packages.
- `harleen_portfolio_backup.csv` – Sample output data for analysis and validation.

## Requirements

Install the following libraries:
- yfinance
- pandas
- requests

## Output

- Ranked dividend yield for all selected stocks.
- Filtered high-yield and sustainable picks.
- Backup CSV data for audit or further analysis.
- Basic validation with a second API (Alpha Vantage).

## Notes

- API rate limits are handled using `time.sleep(1)` between API calls.
- `.get()` method is used instead of `[]` indexing to safely retrieve values from potentially incomplete API responses.
- Defensive coding practices are employed to prevent script failure if any stock data is missing or corrupt.

## Limitations

- This project only uses 5 stocks for demonstration.
- API data may occasionally be inconsistent or delayed.
- The Alpha Vantage free tier may limit validation depth for large portfolios.
