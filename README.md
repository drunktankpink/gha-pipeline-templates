# GitHub Actions Pipeline Templates

Reusable GitHub Action workflows for various technologies.

## Structure

```
.github/workflows/
  terraform/
    validate.yml
    plan.yml
    apply.yml
```

## Usage

You can call any workflow from this repository using `workflow_call`. Example:

```yaml
jobs:
  validate:
    uses: drunktankpink/gha-pipeline-templates/.github/workflows/terraform/validate.yml@main
    with:
      working-directory: ./modules/aws/s3
```