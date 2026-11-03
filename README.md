# sandra-cintel-03-signal-design

[![Python 3.14+](https://img.shields.io/badge/python-3.14%2B-blue?logo=python)](pyproject.toml)
[![CI](https://github.com/sandra8918/sandra-cintel-03-signal-design/actions/workflows/ci-python-zensical.yml/badge.svg)](https://github.com/sandra8918/sandra-cintel-03-signal-design/actions/workflows/ci-python-zensical.yml)
[![Documentation](https://img.shields.io/badge/docs-site-blue?logo=github)](https://sandra8918.github.io/sandra-cintel-03-signal-design/)

[![uv managed](https://img.shields.io/badge/uv-managed-DE5FE9)](https://docs.astral.sh/uv/)
[![ty type checked](https://img.shields.io/badge/ty-type_checked-2F80ED)](https://docs.astral.sh/ty/)
[![Zensical docs](https://img.shields.io/badge/Zensical-docs-purple)](https://zensical.org/)
[![MIT](https://img.shields.io/badge/license-MIT-yellow.svg)](LICENSE)

> Transform raw system measurements into meaningful monitoring signals.

## Project Overview

Author: Sandra Otubushin

Date: 2026-11

This project is a customized starting point for designing useful signals from raw measurements.

The current example demonstrates how raw system measurements can be transformed into error rate, average latency, and throughput.

The planned customization will explore data-submission quality signals using synthetic or public data.

The project is configured in [pyproject.toml](pyproject.toml).

## Data

The current example uses system metrics from `data/`.

Each observation includes:

- `requests` - number of requests handled.
- `errors` - number of failed requests.
- `total_latency_ms` - total response time in milliseconds.

## Approach

The pipeline uses Polars to calculate derived signals:

- **Error rate** - errors relative to requests.
- **Average latency** - average response time per request.
- **Throughput** - request volume represented in the example.

The planned customization may calculate missing-rate, duplicate-rate, error-rate, and an overall data-quality score.

Explore these project components:

- [pyproject.toml](pyproject.toml) - project configuration and dependencies.
- [src/cintel/signal_design.py](src/cintel/signal_design.py) - signal calculations.
- [data/](data/) - input measurements.
- [artifacts/](artifacts/) - generated signals.
- [tests/](tests/) - automated tests.
- [.github/workflows/](.github/workflows/) - automated checks and documentation deployment.
- [docs/](docs/) - project documentation.

## Run the Project

Follow the [Professional Python Workflow Guide](https://denisecase.github.io/pro-analytics-02/) to set up your machine and project environment.

From a VS Code terminal in the project root:

```shell
uv run python -m cintel.signal_design
