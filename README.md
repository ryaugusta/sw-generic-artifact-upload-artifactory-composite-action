# sw-artifact-upload-artifactory-action
Action for uploading generic artifact into Artifactory

### Parameters
| Name | Type |      | Default | Note | 
| ---- | ---- | ---- | ------- | ---- |
`artifact_name` | String | Required* |
`artifactory_secret` | Secret | Required* | `${{ secrets.JF_ARTIFACTORY_TOKEN }}` | Use this org secret
`artifact_path` | String | *Optional* | `${{ github.workspace }}` 
`artifact_repo_name` | String | *Optional* | `third-party-installs`
`artifact_repo_subpath` | String | *Optional* | `${{github.repository}}/${{github.run_number}}`

Usage:
```yaml
    - uses: sherwin-williams-co/sw-generic-artifact-upload-artifactory-action@main
      with:
         artifact_name: <your_artifact_name>
         artifactory_secret: ${{ secrets.JF_ARTIFACTORY_TOKEN }}
         # Optional
         # artifact_path: ${{ github.workspace }}
         # artifactory_repo_name: 'third-party-installs'
         # artifactory_repo_subpath: `${{ github.repository }}/${{ github.run_number }}`
```
