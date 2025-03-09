# Config
My default configurations.

Update repository access for the bots in [GitHub settings](https://github.com/settings/installations).

## Git
The Git config has been supplemented with select options from https://blog.gitbutler.com/how-git-core-devs-configure-git/. The `user.signingkey` option should also be configured with your GPG signing key ID.

Note that the config won't be applied with the `.gitconfig` file in a repository, the contents should be added to `.git/config` within a repository or `~/.gitconfig` to apply globally. 

The Git attributes will apply the specified filters in repositories that it's present in.

Note that the `.gitignore` file is not a template; this is the `.gitignore` for this repository. See https://github.com/github/gitignore for templates. 

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

The label used to denote dependencies is `dependencies`, in colour `#A141FA`.

Note that this sets [`"ignoreTests": true`](https://docs.renovatebot.com/configuration-options/#ignoretests) because 
almost all of my repositories don't have any tests or status checks. Make sure to set this to `false` if you repository does.

Open the [Renovate dashboard](https://developer.mend.io/github/cmenon12) to configure onboarding and view the logs.
