# deployments
Testing GitHub deployments APIs

## Goal

* When a commit is pushed to a branch with an open PR, deploy that commit to an S3 bucket in a directory prefixed with the short SHA of the commit
* When a PR is merged to `master`, deploy that commit to the root of the same S3 bucket as a 'development' deployment
* When a tag is created, deploy that commit to a different S3 bucket as a 'production' deployment
* Use the GitHub [deployments API](https://docs.github.com/en/rest/guides/delivering-deployments) to describe deployments