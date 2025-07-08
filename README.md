# Robust Glasso for High-Dimensional Portfolio Selection

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A robust implementation of Graphical Lasso (Glasso) for portfolio optimization in high-dimensional financial datasets, resistant to outliers and market anomalies.

## 🔍 Overview

This repository contains the code and research for a robust portfolio selection framework that:
- Enhances traditional Glasso with outlier-resistant techniques
- Handles high-dimensional asset universes (100-1000+ assets)
- Improves portfolio performance during extreme market conditions
- Provides sparse network insights into asset relationships

## 🚀 Key Features

- **Robust covariance estimation** using MCD and robust statistics
- **L1-regularized inverse covariance** for sparse portfolio construction
- **Comparative analysis** against traditional Glasso and GAN-based methods
- **Comprehensive backtesting** framework with transaction costs
- **Visualization tools** for portfolio networks and performance

## 📦 Installation

```bash
git clone https://github.com/yourusername/robust-glasso-portfolio.git
cd robust-glasso-portfolio
pip install -r requirements.txt
```

## 🛠️ Usage

```python
from robust_glasso import RobustGraphicalLasso
from portfolio_optimizer import MeanVarianceOptimizer

# Initialize robust glasso
rg = RobustGraphicalLasso(alpha=0.01, robust_threshold=2.5)

# Fit on returns data (assets x observations)
rg.fit(returns_data)

# Get robust precision matrix
precision_matrix = rg.get_precision()

# Optimize portfolio
optimizer = MeanVarianceOptimizer(precision_matrix)
weights = optimizer.maximize_sharpe()
```

## 📊 Results

| Metric          | Traditional Glasso | Robust Glasso |
|-----------------|-------------------|---------------|
| Sharpe Ratio    | 1.2               | 1.5           |
| Max Drawdown    | -25%              | -18%          |
| Out-of-sample R²| 0.65              | 0.78          |

## 📚 Documentation

Full documentation available in the [project thesis](docs/thesis.pdf) (confidential).

## 🤝 Contributing

Academic collaborations welcome through IIT Kharagpur institutional channels.

## 📜 License

MIT License (for code components). Research content remains confidential academic work of IIT Kharagpur.

## 📧 Contact

For academic inquiries: [Institutional Email]@iitkgp.ac.in

---

*Note: This implementation is part of ongoing research at IIT Kharagpur (2023-2024).*
