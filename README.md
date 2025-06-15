# 💧 Water Forecast AI

Water Forecast AI is a project under development focused on data analysis and water consumption forecasting using Artificial Intelligence models.

## 🚀 Features

- **Time series forecasting** with models such as LSTM, ARIMA, and Prophet.
- **Exploratory Data Analysis (EDA)** and signal preprocessing.
- **Evaluation metrics** including MAE, RMSE, and R².
- **Modular structure** for reproducible ML pipelines and experiments.
- **Type-safe Python code** with `mypy` support.
- **Code formatting and linting** with `ruff`.
- **Automated testing** with `pytest` and coverage reporting.
- **Environment and tooling management** via `uv` and `pyproject.toml`.

## ⚙️ Environment Setup

This project uses [`uv`](https://github.com/astral-sh/uv) for Python environment and dependency management.

### Install uv

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

### Create and activate virtual environment

```bash
uv venv .venv
source .venv/bin/activate
```

### Install development dependencies

```bash
uv pip install -e ".[dev]"
```

## 🔒 Dependency Locking

To generate a lockfile for reproducible environments:

```bash
pip-compile pyproject.toml --extra=dev --output-file=requirements.lock.txt
```

This ensures all dependencies (including transitive ones) are pinned and can be synced across environments with full reproducibility.

## 🧪 Running Tests

After activating the virtual environment:

```bash
pytest
```

With coverage report:

```bash
pytest --cov=water_forecast_ai --cov-report=term-missing
```

## 🧹 Code Quality Checks

### Run Ruff (linter & formatter)

```bash
ruff check water_forecast_ai
```

### Run Mypy (type checker)

```bash
mypy water_forecast_ai
```

---
