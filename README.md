# gh-workflows
A collection of reusable GitHub workflows

## Dependecies

### Github App

1. Create a [new GitHub app](https://github.com/settings/apps/new)
  1. Set `https://GitHub.com/apps/<URL name>` as URL
  2. Disable webhooks
2. Create a private key and save it in Bitwarden (or any other secret manager)
3. Remember the App ID

### Adding to a repository
### Set secrets

1. Go to `https://github.com/<your repository>/settings/secrets/actions`
2. Create `ANGELNU_APP_ID` with the App Id from the GitHub app
3. Create `ANGELNU_APP_PRIVATE_KEY` with the App Id from the GitHub app

### Copy required files

- renovate
  1. [schedule-renovate.yaml](.github/workflows/schedule-renovate.yaml)
  2. [renovate.json5](.github/renovate.json5)
     - you need to change the `repositories` section
     - potentially add additional non default rules. See [default renovate config](https://github.com/angelnu/renovate-config).
