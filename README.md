# hello-python 🐍📦

A simple Python CLI application that prints a greeting, OS/architecture info, and an optional sum — with CI/CD powered by ruff, pytest, and PyInstaller.

[![Python CI/CD](https://github.com/TEgor1212/hello-python/actions/workflows/ci.yml/badge.svg)](https://github.com/TEgor1212/hello-python/actions/workflows/ci.yml)

## How to run

Install dependencies and run:

```bash
pip install -r requirements.txt
python app.py
```

Or install the package and use the CLI entry point:

```bash
pip install -e .
hello
```

## CI/CD

On every push to `main`:

- **Lint:** `ruff check .` + `ruff format --check .`
- **Test:** `pytest -v`

On pushing a tag `v*`:

- **PyInstaller** builds a standalone executable on Linux, macOS, and Windows
- **Artifacts** are uploaded to GitHub Releases:
  - `hello-python-linux-x64`
  - `hello-python-macos-arm64`
  - `hello-python-windows-x64.exe`