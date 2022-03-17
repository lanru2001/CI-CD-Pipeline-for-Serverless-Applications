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

![image](https://user-images.githubusercontent.com/59709429/158893058-ec11852f-927c-4146-b9d8-812cb62c45f9.png)

Serverless Applications

Serverless is a concept for operating cloud applications in comparison to VM based or container based architectures. The code is executed by Function-as-a-Service (FaaS) services like AWS Lambda. You only provide your source code (think NodeJs files and libraries). AWS takes care of the execution, scaling and so on. But FaaS is only the core offering of Serverless. The idea of Serverless architectures is using additional services like S3 for storage, DynamoDB as a database, Cognito for user management and so on. All these services scale with your demand, you only pay for used resources (not for idle) and they are all operated by your cloud vendor, e.g. AWS.
Serverless applications can be a cost saver, but above all, they remove most of the operational complexity. Serverless allows writing cloud applications with high availability and scalability easily.


Serverless Architecture

![image](https://user-images.githubusercontent.com/59709429/158893427-8c8c3e62-6e2f-4206-be54-576f31c8ca42.png)

Source:https://medium.com/@tarekbecker/a-production-grade-ci-cd-pipeline-for-serverless-applications-888668bcfe04
