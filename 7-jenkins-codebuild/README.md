# Usage

* Gather CodeBuild service IP range from  [https://ip-ranges.amazonaws.com/ip-ranges.json](here) in case you want to allow that in RDS or any other security group to make the build process successful.
* Create IAM group with  AmazonS3FullAccess, AWSCodeBuildDeveloperAccess  policy attached.
* Create IAM user with programmatic access in AWS and assign the user the above group.
* Create IAM role with policies in the repository.
* Install AWS CodeBuild plugin in Jenkins.
* Create Jenkins credential as a CodeBuild Credentials type with IAM user access key ID and secret key.
* Use IAM role ARN in advanced section of jenkins credential and make sure that no error appears in Jenkins.
* Keep the Jenkinsfile and buildspec.yml in the root of the project.
* Test project build from CodeBuild.
* Change appropriate values in policies, Jenkinsfile according to your configuration.

# Help

* You can get the AWS account ID either from console or aws cli. To get from CLI implement the following command,

```shell
aws sts get-caller-identity --output text --query 'Account'
```

