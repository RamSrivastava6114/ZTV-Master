# ZVT-MASTER

<!-- Additional Shields for ZVT-MASTER -->

![Downloads](https://img.shields.io/pypi/dm/zvt-master?style=for-the-badge&color=2563EB)
![Python Versions](https://img.shields.io/pypi/pyversions/zvt-master?style=for-the-badge&color=306998)
![GitHub Stars](https://img.shields.io/github/stars/RamSrivastava6114/ZTV-Master?style=for-the-badge&color=F1C40F)
![GitHub Forks](https://img.shields.io/github/forks/RamSrivastava6114/ZTV-Master?style=for-the-badge&color=7DCEA0)
![Open Issues](https://img.shields.io/github/issues/RamSrivastava6114/ZTV-Master?style=for-the-badge&color=E74C3C)
![Contributors](https://img.shields.io/github/contributors/RamSrivastava6114/ZTV-Master?style=for-the-badge&color=9B59B6)
![Latest Commit](https://img.shields.io/github/last-commit/RamSrivastava6114/ZTV-Master?style=for-the-badge&color=16A085)


> **ZVT-MASTER** is a modular Python-based backtesting framework for analyzing trading strategies on time-series financial data.

---

## 📚 Table of Contents

- [✨ Features](#-features)  
- [🧱 Architecture](#-architecture)  
- [🔁 Flowchart](#-flowchart)  
- [🛠 Installation](#-installation)  
- [🚀 Usage](#-usage)  
- [🧪 Testing](#-testing)  
- [📊 Screenshots](#-screenshots)  
- [📂 File Structure](#-file-structure)  
- [📦 Modules Overview](#-modules-overview)  
- [🧩 Sample Strategies](#-sample-strategies)  
- [🤝 Contributing](#-contributing)  
- [🪪 License](#-license)  
- [📬 Contact](#-contact)  

---

## ✨ Features

- 📈 Strategy plug-and-play framework  
- 🧠 Support for technical indicators & machine learning  
- 🕒 Custom date filtering, trading window support  
- ⚙️ Multi-asset and multi-timeframe support  
- 📦 Compatible with CSV, SQL, APIs  
- 📊 Generates detailed metrics and visualizations  
- 📚 Fully testable with PyTest and coverage tools  

---

## 🧱 Architecture

```mermaid
sequenceDiagram
    participant UI as User Interface (CLI/Notebook/API)
    participant SE as Strategy Engine
    participant BE as Backtest Engine
    participant DL as Data Loader
    participant OB as Order Book Simulator
    participant PR as Performance Reporter

    UI->>SE: load strategy
    SE->>SE: validate strategy
    SE-->>BE: execute strategy
    BE->>DL: fetch data (csv/api/db)
    DL-->>BE: return time‑series data
    BE->>OB: simulate order book
    OB-->>BE: return fills & trades
    BE->>PR: calculate metrics & reports
    PR-->>UI: present results & visualizations

```
### Flowchart

```mermaid
flowchart TD
    A[User Input] --> B[Data Loader]
    B --> C[Preprocessing]
    C --> D[Strategy Engine]
    D --> E[Backtester]
    E --> F[Performance Analyzer]
    F --> G[Visualization & Report]
```

### Installation

# Clone the repository
```bash
git clone https://github.com/yourusername/ZVT-MASTER.git
cd ZVT-MASTER
```
# Create a virtual environment
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

# Install dependencies
```bash
pip install -r requirements.txt
pip install .
```

### Usage
Basic Python Usage
python
Copy
Edit

```python
from zvt_master import BacktestEngine

engine = BacktestEngine(
    data_source="data/BTC_USD.csv",
    strategy="examples/moving_average.py",
    initial_capital=100000
)
results = engine.run()
engine.plot(results)
```
### Cli Use
```bash
python run_once.py --data data/SPY.csv --strategy examples/macrossover.py
```

### File Structure
```bash
ZVT-MASTER/
├── .github/workflows/       → CI/CD configs
├── api-tests/               → API validation tests
├── docs/                    → Documentation and diagrams
├── examples/                → Strategy examples
├── requirements/            → Optional dependency groups
├── sql/                     → Database schema/scripts
├── src/                     → Core application source
│   ├── engine/              → Backtesting logic
│   ├── strategy/            → Strategy templates
│   └── metrics/             → Reports and metrics
├── tests/                   → Unit/integration tests
├── .coveragerc              → Coverage config
├── build.sh                 → Build script
├── code_of_conduct.md       → Contributor guidelines
├── init_env.sh              → Dev environment setup
├── LICENSE                  → License file
├── MANIFEST.in              → Manifest
├── pyproject.toml           → Python packaging config
├── requirements.txt         → Base dependencies
└── setup.py                 → Setup script
```

### To Contribute


# Fork the repo
```bash
git clone https://github.com/yourusername/ZVT-MASTER.git
```
# Create a feature branch
```bash
git checkout -b feature/my-feature
```
# Commit your changes
```bash
git commit -m "feat: Add my feature"
```
# Push and open a PR
```bash
git push origin feature/my-feature
```
