# DataLib

[![CI](https://github.com/stormynight9/datalib/actions/workflows/ci.yml/badge.svg)](https://github.com/stormynight9/datalib/actions/workflows/ci.yml)
[![PyPI version](https://badge.fury.io/py/nf-datalib.svg)](https://badge.fury.io/py/nf-datalib)
[![Python Version](https://img.shields.io/pypi/pyversions/nf-datalib.svg)](https://pypi.org/project/nf-datalib/)

A Python library for data manipulation and analysis, with comprehensive test coverage and continuous integration.

## Installation

You can install DataLib using pip:

```bash
pip install nf-datalib
```

## Features

### Data Manipulation

- Load and process CSV files (read, write, filters).
- Data transformations (normalization, handling missing values).

### Statistical Computations

- Mean, median, mode, standard deviation, correlation.
- Basic statistical tests (t-test, chi-square test).

### Data Visualization

- Generate simple graphs (bar charts, histograms, scatter plots).
- Support for advanced visualizations like correlation matrices.

### Advanced Analysis

- Linear and polynomial regression models.
- Supervised classification algorithms (k-NN, decision trees).
- Unsupervised methods (k-means, principal component analysis).

## Usage

Here's a quick example of how to use DataLib:

```python
from datalib.data_manipulation import normalize_column
from datalib.visualization import plot_histogram
import pandas as pd

# Load and normalize data
data = pd.DataFrame({"values": [1, 2, 3, 4, 5]})
normalized = normalize_column(data, "values", method="minmax")

# Create visualization
fig = plot_histogram(data, "values")
fig.savefig("histogram.png")
```

## Development

To set up the development environment:

1. Clone the repository:

   ```bash
   git clone https://github.com/stormynight9/datalib.git
   cd datalib
   ```

2. Install development dependencies:

   ```bash
   pip install -e ".[test,doc]"
   ```

3. Run tests:

   ```bash
   pytest tests/
   ```

4. Build documentation:
   ```bash
   cd docs
   make html
   ```

## Versioning

This project uses [Semantic Versioning](https://semver.org/). For the versions available, see the [tags on this repository](https://github.com/stormynight9/datalib/tags).

To create a new release:

```bash
python scripts/release.py [major|minor|patch]
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Author

- **Nader Ferjani** - [GitHub](https://github.com/stormynight9)
- Email: ferjani.nader@hotmail.fr

---

## Project Goals

The main objective is to develop a professional packaging system for the DataLib library, enabling:

1. Easy and intuitive installation through package managers like `pip`.
2. Distribution on platforms like PyPI (Python Package Index).
3. Integrated, clear, and accessible documentation.

---

## Work Plan

### 1. Project Structure

- Organize the source code in a modular format (e.g., `src/` directory).
- Define essential files like `setup.py`, `pyproject.toml`, or `setup.cfg`.

### 2. Dependencies and Compatibility

- Identify and include necessary dependencies (e.g., `numpy`, `pandas`, `matplotlib`, `scikit-learn`).
- Ensure compatibility with recent Python versions.

### 3. Documentation

- Write a detailed `README.md` or `README.rst` outlining the library's usage and features.
- Add concrete usage examples.
- Generate technical documentation using tools like Sphinx.

### 4. Testing

- Write unit tests for main functions using `pytest`.
- Integrate CI/CD workflows (e.g., GitHub Actions) to validate changes.

### 5. Publication

- Prepare and publish the library on PyPI.
- Regularly update the version following semantic versioning (SemVer).

---

## Deliverables

- A functional library distributable via `pip`.
- Online documentation (e.g., hosted on Read the Docs).
- Automated tests and code quality monitoring.

---

## Evaluation Criteria

- **Packaging Quality**: Ease of installation and compatibility.
- **Documentation Clarity**: Completeness and ease of understanding.
- **Functionality and Robustness**: Reliability of the library's tools.
- **Test Coverage**: Quality and extent of automated testing.

---

DataLib aims to become a reliable and user-friendly library for data enthusiasts and professionals alike, enhancing the Python data ecosystem.
