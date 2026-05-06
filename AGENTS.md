# AGENTS.md — GEOIT1501 website

This is a **Sphinx** documentation site for a TU Delft MSc Geomatics course. All content is MyST Markdown (`.md`). No application code, no tests, no linters, no CI.

## Commands

```sh
uv sync                          # install dependencies
mkdir _build                     # required before first build
uv run sphinx-autobuild src _build   # dev server → http://127.0.0.1:8000
sphinx-build src _build          # one-off HTML build (deploy step)
```

The auto-generated `Makefile` at repo root is **not used** — `SOURCEDIR = .` is wrong for this layout. Always use the commands above.

## Deploy

```sh
./deploy.sh    # not tracked in git; builds + rsyncs to geomatics01
```

## Key facts

- **Package manager**: `uv` (not pip). `requirements.txt` is legacy/unused.
- **Theme**: Furo. Config in `src/conf.py`.
- **Extensions**: `myst_parser`, `sphinx_copybutton`, `sphinx_design`, `sphinx.ext.autodoc`, `sphinx.ext.extlinks`.
- **MyST extensions enabled**: `colon_fence`, `deflist`.
- **Octicons** are used inline (e.g. `{octicon}`home`{/octicon}`).
- **No CI/CD**, no pre-commit, no formatter, no test framework.
- **`deploy.sh` is gitignored** — you cannot read it from git; its content is one `sphinx-build src _build` + one `rsync` to the server.
- **`.python-version`**: 3.13.
