# Config
My default configurations.

Update repository access for the bots in [GitHub settings](https://github.com/settings/installations).

This is a test of in-solidarity, not to be merged. Master. He does the work. Hallucination.

## In Solidarity
This config is based on guides from [ietf/terminology](https://github.com/ietf/terminology) and the [Inclusive Naming 
Initiative](https://www.inclusivenaming.org).

Use this in another repo by adding the code below to `.github/in-solidarity.yml`.
```yaml
_extends: cmenon12/config
```

## Renovate
See the [Renovate documentation](https://docs.renovatebot.com/configuration-options/) for available options.

Use this in another repo by adding the code below to `renovate.json`.
```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": [
    "github>cmenon12/config(your-repo-slug)"
  ]
}
```

Note that this sets [`"ignoreTests": true`](https://docs.renovatebot.com/configuration-options/#ignoretests) because 
almost all of my repositories don't have any tests or status checks. Make sure to set this to `false` if you repository does.

Open the [Renovate dashboard](https://developer.mend.io/github/cmenon12) to configure onboarding and view the logs.
