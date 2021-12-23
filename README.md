# Ale Github Actions - Connect Repository

Performs the necessary setup tasks such as adding a Deploy Key to allow Ale to access your GitHub repository within its space (Scope).

## Inputs

## `endpoint`

**Required** Ale API Endpoint

## `token`

**Required** Ale API Key

## `ghtoken`
**Required** A GitHub Personal Access Token with read/write permissions for managing Deploy Keys.

## `repo`
The GitHub repository in the format: `user/repo`.  
Defaults to the current repository: `${{ github.repository }}`.

## `scope`
The Ale scope to connect to. This can be a user or team name.

## `readOnly`
If set to `true`, the Deploy Key will be created with read-only permissions.  
Defaults to `false`.


---

## Usage Examples


```yaml
uses: ale-run/github-actions-connect@v1
with:
  endpoint: ${{ secrets.ALE_ENDPOINT }}
  token: ${{ secrets.ALE_TOKEN }}
```


```yaml
uses: ale-run/github-actions-connect@v1
with:
  endpoint: ${{ secrets.ALE_ENDPOINT }}
  token: ${{ secrets.ALE_TOKEN }}
  ghtoken: ${{ secrets.GITHUB_TOKEN }}
  repo: ${{ github.repository }}
  readOnly: true
```

