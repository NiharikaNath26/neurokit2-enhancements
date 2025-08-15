
# NeuroKit2 Enhancements – Turing Practice Task

This repository documents enhancements made to the [NeuroKit2](https://github.com/neuropsychology/NeuroKit) open-source project as part of the Turing Practice Task Assessment. The goal was to demonstrate production-level engineering by analyzing a real Python codebase, identifying improvement opportunities, and delivering tested, high-quality enhancements.

---

## 🚀 Project Overview

**Original Repository**: [neuropsychology/NeuroKit](https://github.com/neuropsychology/NeuroKit)  
**Language**: Python  
**Stars**: ~1.9K  
**Domain**: Neurophysiological Signal Processing (ECG, EDA, RSP, etc.)

---

## ✅ Enhancements Implemented

### 1. 🧵 Asynchronous Signal Processing
- Converted `bio_process()` and related signal functions to support `async`/`await`.
- Enabled non-blocking, real-time processing for streaming use cases.
- Backward-compatible with existing synchronous workflows.

### 2. 🖥️ Command-Line Interface (CLI)
- Added a `cli.py` module using `argparse`.
- Enables users to process signals via terminal with commands like:
  ```bash
  python cli.py --input data.csv --output results.csv --signals ecg eda
  ```

### 3. 🔁 Shared Signal Utilities Refactor
- Extracted common functions (e.g., normalize, resample) into a shared module.
- Reduced code duplication and improved maintainability across signal types.

---

## 📂 Directory Structure

```
.
├── shared/                     # Common signal utilities
├── cli.py                      # Command-line interface
├── tests/                      # Unit and async tests
├── .pylintrc                   # Linting config
├── .coveragerc                 # Coverage config
├── reports/
│   ├── NeuroKit2_Technical_Assessment_Report.md
│   ├── NeuroKit2_Prompt_Portfolio.md
│   ├── NeuroKit2_Implementation_Report.md
│   ├── NeuroKit2_Test_Execution.txt
│   ├── NeuroKit2_Coverage_Report.html
│   ├── NeuroKit2_Submission_Template.csv
```

---

## 🧪 Testing & Quality Assurance

- Framework: `pytest` with `pytest-cov` and `pytest-asyncio`
- Test Coverage: >90% for new code
- Static Analysis: Configured with `pylint`
- Linting rules: See `.pylintrc`

---

## 📊 Reports

| Report Type        | File |
|--------------------|------|
| Technical Report   | `NeuroKit2_Technical_Assessment_Report.md` |
| Enhancement Prompts | `NeuroKit2_Prompt_Portfolio.md` |
| Implementation Details | `NeuroKit2_Implementation_Report.md` |
| Coverage Report    | `NeuroKit2_Coverage_Report.html` |
| Linting Rules      | `.pylintrc` |
| Submission Sheet   | `NeuroKit2_Submission_Template.csv` |

---

## 📌 How to Use

Install dependencies:

```bash
pip install -r requirements.txt
```

Run CLI:

```bash
python cli.py --input example.csv --output features.csv --signals ecg eda
```

Run tests:

```bash
pytest --cov=shared tests/
```

---

## 📫 Contact

Created as part of Turing onboarding. Maintained by [Your Name / Email Here].
