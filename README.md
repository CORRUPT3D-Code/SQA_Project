# SQA Project

## Usage

### Run using uv

Install [`uv`](https://docs.astral.sh/uv/getting-started/installation/#installation-methods) (Python ≥ 3.14 required).

```bash
git clone https://github.com/Corrupted-Code/SQA_Project.git
cd SQA_Project
uv run sqa server start
```

Once the server is up, open http://localhost in your browser.

## Development

### Setup

```bash
uv run poe setup
```

This runs `uv sync --all-groups` to install all dependencies including dev and lint extras.

### Building

#### Wheel

```bash
uv build
```

Produces a `.whl` file suitable for distribution via `uvx`.

#### Standalone executable

Requires one of the [C compilers supported by Nuitka](https://github.com/Nuitka/Nuitka?tab=readme-ov-file#c-compiler).

```bash
uv run poe build
```

### Testing

```bash
uv run pytest
```

Tests run in parallel across all available CPU cores via `pytest-xdist`.

### Formatting

```bash
uv run poe format          # format entire project
uv run poe format -- path  # format a specific path
```

### Clean

Remove all temporary and generated files:

```bash
uv run poe clean
```
