# deploy-cdn

Deply to A-dapt CDN's

## Inputs

### `artefact-bucket`

**Required** Name of the S3 bucket for deployment artefacts

### `aws-region`

**Optional**

### `prefix`

**Optional** S3 bucket key prefix for files to deploy, defaults to none

### `files-to-deploy`

**Required** List of files to deploy separated by newlines

### `release`

**Required** Semantic versioning for release to deploy

### `role-to-assume`

**Required** ARN of the role to assume for deployment

## Example usage

```
uses: A-dapt/deploy-cdn@v1.0
with:
  release: ${{ env.RELEASE }}
  files-to-deploy: |
    sdk.js
    sdk.css
  artefact-bucket: ${{ secrets.ADAPT_DEPLOYMENT_ARTEFACTS }}
  role-to-assume: ${{ secrets.AWS_ROLE_TO_ASSUME_ADAPT_CORE_PLATFORM }}
```

## TODO (Future versions)
