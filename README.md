All in all, at least the following steps are required. Of course there can be reasons to include more steps.
testing every commit (or pull request) before merging to master
executing unit tests, code checks and so on
running integration tests with other services in a QA environment
optionally deploying to staging (only on master branch)
deploying to production (only on master branch)
automatically rollbacking in case of failure during deployment
all steps above must be completely automated
Below, you can see an overview of the pipeline we want to build.

Overview of the target pipeline
