# Linux RISC-V Github Helpers

Collection of tools to manage the linux-riscv GH repo.

## Install

Old school Python install

```
python -m venv .venv
. .venv/bin/activate
pip install -r requirements.txt
```

## Typical usage

List all failing tests (series is the big suite) for upstream branches:
```
. .venv/bin/activate
export GH_TOKEN='ghp_YaddaYadda'
./ghpr --upstream-prs --series-workflow
```

List all tests (series is the big suite) for upstream branches:
```
. .venv/bin/activate
export GH_TOKEN='ghp_YaddaYadda'
./ghpr --upstream-prs --series-workflow --all-results
```

List all failing tests for patchwork series:
```
. .venv/bin/activate
export GH_TOKEN='ghp_YaddaYadda'
./ghpr --patches-workflow
```

Use `--pr` to select one or more PRs. If not passed, all PRs are
returned.
