---
title: uv
tags:
- cli
- input-file
- eval-py
references:
- https://docs.astral.sh/uv/pip/compatibility/
- https://docs.astral.sh/uv/concepts/configuration-files/
files: [requirements.txt, constraints.txt, setup.py, pyproject.toml, uv.toml]
---

# uv
`uv` is a Python package installer and resolver. 

## uv pip 

The LOTPs defined for pip also apply to `uv` with `uv pip install`. 

See [pip LOTP article](pip.md). 

## uv-specific configuration files
Furthermore, `uv` follows the configurations defined in `uv.toml` and in the [[tool.uv]] sections of the `pyproject.toml` file. If both toml files are present, only `uv.toml` will be taken into account. If `uv.toml` exists but is empty, the default configurations of `uv` will be used and `pyproject.toml` will be ignored. 

It is possible to configure `index-url` and `extra-index-url` in the previous files, thereby redirecting the source of the packages to be downloaded to a source controlled by an attacker. 