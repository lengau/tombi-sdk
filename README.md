# tombi SDK for Workshop

A development environment for projects that use [tombi](https://github.com/tombi-toml/tombi),
a TOML Formatter, Linter, and Language Server. It installs the `tombi`
binary on the workshop PATH so you can format, lint, and validate TOML files
inside the workshop.

---

## Reference workshop

A minimal workshop:

```yaml
# workshop.yaml
name: dev
base: ubuntu@24.04
sdks:
  - name: tombi
    channel: 1.11/stable
```

This demonstrates a basic setup where `tombi` is available for running
TOML formatting and linting.

---

## Using the SDK

### Prerequisites, project layout

1. The project repository is mounted at `/project` inside the workshop, as
   with any workshop.
2. A `tombi.toml` or `pyproject.toml` in the project root can configure `tombi`.
   See the [upstream documentation](https://tombi-toml.github.io/tombi).

### Format and lint TOML files

Once the workshop is ready:

```bash
workshop exec -- tombi format
workshop exec -- tombi lint
```

or, from within the workshop shell:

```bash
workshop shell
tombi format
tombi lint
```

---

## Plugs (resources this SDK consumes)

This SDK doesn't define any plugs.

## Slots (resources this SDK provides)

This SDK doesn't define any slots.

---

## Documentation and guidance

- [tombi official documentation](https://tombi-toml.github.io/tombi)
- [tombi source repository](https://github.com/tombi-toml/tombi)

---

## Community and support

- Workshop community on [Matrix](https://matrix.to/#/#documentation:ubuntu.com)
  and [Discourse](https://discourse.ubuntu.com/)
- Please review our [Code of Conduct](https://ubuntu.com/community/ethos/code-of-conduct)
  before participating.

---

## Contributions

All contributions, including code, documentation updates, and issue reports,
are welcome!

- Open issues or pull requests on the repository you obtained this SDK from.

---

## License and copyright

Copyright 2026 Alex Lowe.

The tombi SDK is released under the MIT License. The packaged `tombi` binary is
released under its upstream license; see
https://github.com/tombi-toml/tombi/blob/main/LICENSE for details.
