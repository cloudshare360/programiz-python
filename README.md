# Installing Python requirements

This project lists Python dependencies in `requirements.txt`. Recommended methods to install them:

1) Recommended — create and use a virtual environment (isolated, safe)

```bash
python3 -m venv .venv
source .venv/bin/activate    # Windows: .venv\Scripts\activate
python -m pip install --upgrade pip
pip install -r requirements.txt
```

2) If you cannot create a venv, install for the current user (no sudo)

```bash
python3 -m pip install --user --upgrade pip
python3 -m pip install --user -r requirements.txt
```

3) Using the Dev Container (recommended for consistent environment)

- Open this repository in VS Code and choose "Reopen in Container" or run:

```bash
devcontainer rebuild .
```

The devcontainer `postCreateCommand` will install `requirements.txt` for you.

Notes
- If your system Python is externally managed (PEP 668), prefer a virtualenv.
- On Alpine or other minimal distros, you may need `apk add py3-venv py3-pip` first.
- After installing, run tests with `pytest` (or `.venv/bin/pytest` when not activated).
