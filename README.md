# For testing github actions

## Pre-Commit Hooks

For proper linting and checking, this repo uses `pre-commit` associated with `pre-push` hooks. The following must be installed in the local workstation. See [Confining Hooks to Run at Certain Stages](https://pre-commit.com/#confining-hooks-to-run-at-certain-stages) for details.

* [pre-commit](https://pre-commit.com/)
* [checkov](https://github.com/bridgecrewio/checkov)
* [cfn-lint](https://github.com/aws-cloudformation/cfn-lint)

After the first checkout locally, run the following command to initial the pre-commit hooks.

```bash
pre-commit install --hook-type pre-push
```

It is possible to run the pre-commit hooks manually. To run all the pre-commit hooks for this repo, run

```bash
pre-commit run --all-files
```

To run just the Cloudformation linter (`cfn-lint`), run

```bash
pre-commit run cfn-python-lint
```

To run just the checkov checker, run

```bash
pre-commit run checkov
```

<!-- BEGIN_TF_DOCS -->
## Requirements

| Name | Version |
|------|---------|
| terraform | ~> 1.2 |

## Providers

No providers.

## Modules

No modules.

## Resources

No resources.

## Inputs

No inputs.

## Outputs

No outputs.
<!-- END_TF_DOCS -->