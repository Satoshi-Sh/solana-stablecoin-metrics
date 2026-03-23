# Solana Data Benchmark
An open-source benchmarking tool that pulls KPI data from multiple providers in the Solana ecosystem. If you doubt the data from a certain provider, you can verify it against others at [solana.com/data](https://solana.com/data).

## Why This Exists
Different data providers often report different numbers for the same metric. Which one is right? Instead of trusting a single source, this project aggregates data from multiple providers so you can compare them and spot discrepancies. 

It's built for Solana with cross-provider benchmarking.

## Supported Providers
| Provider | API Key Required | Status |
|----------|-----------------|--------|
| [Allium](https://allium.so) | Yes | Planned |
| [Artemis](https://artemis.xyz) | Yes | Planned |
| [Blockworks Research](https://blockworksresearch.com) | Yes | Planned |
| [DefiLlama](https://defillama.com) | Yes | Planned |
| [Dune](https://dune.com) | Yes | Planned |
Want to add a provider? See [Adding a New Provider](#adding-a-new-provider).

## Suported KPIs

### Stablecoins
| Metric | Unit | Description |
|--------|------|-------------|
| Supply | USD | Total circulating supply of stablecoins on Solana, denominated in USD |
| Transfer Volume | USD | Total transfer volume of stablecoins on Solana, denominated in USD |
| Transfer Count | Count | Total number of stablecoin transfer transactions on Solana |
| Active Addresses | Count | Number of unique addresses interacting with stablecoins on Solana |


## Tech Stack

- **Python 3.10+**
- **Databricks** for data storage and processing
- **Provider APIs** for data ingestion

## Getting Started

### Prerequisites

- Python 3.10 or higher
- Access to a Databricks workspace
- API keys for the providers you want to use

### Installation

```bash
git clone https://github.com/Satoshi-Sh/solana-stablecoin-metrics
cd solana-data-benchmark
pip install -r requirements.txt
```

### Configuration
1. Copy the example environment file: 
```bash
cp .env.example .env
```

2. Fill in your API keys and Databricks connection details:
```
ALLIUM_API_KEY=your_key_here
ARTEMIS_API_KEY=your_key_here
BLOCKWORKS_API_KEY=your_key_here
DUNE_API_KEY=your_key_here
DATABRICKS_CATALOG=your_catalog_name
DATABRICKS_SCHEMA=your_schema_name
```

3. Run the application:
```bash
python main.py
```

## Adding a New Provider

## Adding a New Metric

## Contributing 

Contributions are welcome! Whether it's adding a new data provider, a new metric, or improving the comparison logic — open an issue or submit a PR.