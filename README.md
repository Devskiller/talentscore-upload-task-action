# DevSkiller TalentScore - Upload task action

This GitHub Action uploads custom programming tasks to the DevSkiller TalentScore platform. It allows you to easily integrate the upload process into your CI/CD pipeline.

## Inputs

### `api_key`
**Required**: The TalentScore API key. This key is needed to authenticate the upload request.

### `path`
**Required**: The path to the programming task directory that contains the task source code to upload.

### `id`
**Optional**: The ID of the programming task you want to update on the TalentScore platform. If not provided, the code task directory should contain a [metadata.yaml file](metadata-file-structure.md).

### `publish`
**Optional**: If set to `true` (default), the task will be published automatically after a successful build.

## Example

```yaml
name: Sample task upload

on:
  push:
    branches:
      - master

jobs:
  upload-task:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v2
      - uses: Devskiller/talentscore-upload-task-action@v1.0.0
        with:
          api_key: ${{ secrets.TALENTSCORE_API_KEY }}
          id: fe3217a6-e085-47dd-afff-025be5355d87
          path: ./src
```

## How to prepare a custom programming task
Please see: [Creating custom tasks](https://help.devskiller.com/space/TSG/2893873179/Creating+Custom+Tasks)