# Github

## Branch Protection Rules

This will create the default branch protection rules using github API.

```
./branch-protection.sh $reponame $PAT
```

PAT must have `administration:write`. https://docs.github.com/en/rest/repos/rules?apiVersion=2022-11-28#create-a-repository-ruleset
