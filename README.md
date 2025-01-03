# PyABTest

A comprehensive Python library for designing, analyzing, and validating A/B tests. PyABTest provides a collection of statistical tools and utilities to help you make data-driven decisions through experimentation.

## Features

- **Hypothesis Testing & Power Analysis**
  - Sample size calculation
  - Power analysis
  - Effect size calculations (Cohen's d, h)
  - Multiple comparison adjustments

- **Statistical Analysis**
  - Proportion-based tests (z-tests)
  - Mean-based tests (t-tests)
  - Non-parametric tests (Mann-Whitney U)
  - Confidence interval calculations
  - Ratio metrics analysis with Delta method

- **Validation Tools**
  - Sample Ratio Mismatch (SRM) detection
  - A/A test functionality
  - Novelty effect detection
  - Simpson's paradox checks
  - Data quality validation

- **Metrics & Analysis**
  - Conversion rate analysis
  - Click-through rate calculations
  - Revenue metrics
  - Custom metric definitions
  - Ratio metrics with variance estimation

- **Visualization**
  - Distribution plots
  - Time series analysis
  - Effect size visualization
  - Power curves

## Installation

```bash
pip install pyabtest
```

## Quick Start

```python
import pyabtest as ab

# Calculate required sample size
sample_size = ab.hypothesis.calculate_sample_size(
    effect_size=0.1,
    power=0.8,
    alpha=0.05
)

# Perform z-test for proportions
result = ab.analysis.proportion_test(
    control_conversions=100,
    control_size=1000,
    treatment_conversions=120,
    treatment_size=1000
)

# Check for Sample Ratio Mismatch
srm_result = ab.validation.check_srm(
    control_size=1000,
    treatment_size=1050,
    expected_ratio=0.5
)

# Analyze ratio metrics
ratio_test = ab.metrics.delta_method_test(
    control_numerator=revenue_control,
    control_denominator=users_control,
    treatment_numerator=revenue_treatment,
    treatment_denominator=users_treatment
)
```

## Documentation

For detailed documentation, visit [docs.pyabtest.io](https://docs.pyabtest.io)

### Examples

The `examples/` directory contains Jupyter notebooks demonstrating:
- Basic A/B test analysis
- Sample size calculation
- Metric analysis
- Validation techniques
- Visualization examples

## Requirements

- Python ≥ 3.8
- numpy
- scipy
- statsmodels
- pandas
- matplotlib
- seaborn
- pingouin

## Contributing

We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for details.

### Development Setup

```bash
# Clone the repository
git clone https://github.com/yourusername/pyabtest.git
cd pyabtest

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install development dependencies
pip install -r requirements-dev.txt

# Run tests
pytest
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Citation

If you use PyABTest in your research, please cite:

```bibtex
@software{pyabtest2024,
  author = Siddhant Maharana,
  title = {PyABTest: A Python Library for A/B Testing},
  year = {2024},
  url = {https://github.com/yourusername/pyabtest}
}
```

## Acknowledgments

Special thanks to all contributors and the A/B testing community for inspiration and feedback.