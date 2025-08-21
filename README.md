# getBISy

A Python package for programmatically fetching and working with Bank for International Settlements (BIS) datasets, including policy rates, exchange rates, locational banking statistics, international debt securities, and global liquidity data.

## Features
- Fetch policy rate data for any country and frequency
- Retrieve exchange rate data for any currency
- Access locational banking statistics with flexible filters
- Download international debt securities data
- Obtain global liquidity data
- Enum-based API for robust, error-resistant parameterization

## Installation

Clone the repository and install dependencies:

```bash
pip install -r requirements.txt
```

## Usage

Import the data functions and enums you need:

```python
from src.data import get_policy_rate_data, get_exchange_rate_data, get_locational_banking_data
from src.enums import LbsMeasure, Position, Instrument, CurrencyType, Institution, Sector, Region, PositionType

# Example: Fetch policy rate data
rates = get_policy_rate_data('US', 'M')

# Example: Fetch exchange rate data
fx = get_exchange_rate_data('USD')

# Example: Fetch locational banking data
lbs = get_locational_banking_data(measure=LbsMeasure.Stocks, position=Position.Claims)
```

## Enum Reference
All major parameters are type-safe enums, defined in `src/enums.py`. Example enums include:
- `LbsMeasure`, `Position`, `Instrument`, `CurrencyType`, `Institution`, `Sector`, `Region`, `PositionType`, `CurrencyGroup`, `Maturity`, `RateType`, `IdsMeasure`, `UnitOfMeasure`

## Project Structure
```
getBISy/
├── src/
│   ├── __init__.py
│   ├── data.py         # Main data-fetching functions
│   ├── enums.py        # Enum definitions for all API parameters
│   ├── fetcher.py      # Fetcher classes for making API requests
│   └── ...
├── requirements.txt
```
