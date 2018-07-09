# Usage

* Remember CodeBuild, S3 must reside under same region when it comes to upload artifacts.
* Gather CodeBuild service IP range from  [https://ip-ranges.amazonaws.com/ip-ranges.json](here) in case you want to allow that in RDS or any other security group to make the build process successful.
* Create IAM group with  AmazonS3FullAccess (optional), AWSCodeBuildDeveloperAccess  policy attached.
* Create IAM user with programmatic access in AWS and assign the user the above group.
* Generate IAM user access key id and secret key. Note them down for later use.
* Create IAM role with policies in the repository. See in #Help section.
* Install AWS CodeBuild plugin in Jenkins.
* Create Jenkins credential as a CodeBuild Credentials type with IAM user access key ID and secret key.
* Use IAM role ARN in advanced section of jenkins credential and make sure that no error appears in Jenkins.
* Keep the Jenkinsfile and buildspec.yml in the root of the project.
* Test project build from CodeBuild or from Jenkins project build. You will get project build log directly in Jenkins!
* Change appropriate values in policies, Jenkinsfile according to your configuration.

# Help

* You can get the AWS account ID either from console or aws cli. To get from CLI implement the following command,

```shell
aws sts get-caller-identity --output text --query 'Account'
```

* Create IAM role with policies in the following way,

```shell
cd iam-codebuild-role-policy/
aws iam create-role --role-name CodeBuildServiceRole --assume-role-policy-document file://create-role.json
aws iam put-role-policy --role-name CodeBuildServiceRole --policy-name CodeBuildServiceRolePolicy --policy-document file://put-role-policy.json
```
