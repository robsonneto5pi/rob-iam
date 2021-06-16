# rob-iam
Curriculum vitae - Carreira de vida

- rob: Robson de Oliveira Neto
- iam: Carreira de vida

1. Task - Creating an S3 bucket

AWS Tools for PowerShell

````
$MYBUCKET= Read-Host -Prompt 'Please enter a bucket name' ; New-S3Bucket -BucketName $MYBUCKET
````

2. Task - Copy all the contents of the rob-iam folder to Amazon S3

````
Write-S3Object `
  -BucketName $MYBUCKET `
  -KeyPrefix rob-iam `
  -Folder rob-iam `
  -CannedACLName public-read `
  -Recurse
````

3. Task - Use Write-Host to build the URL to your web application

````
Write-Host https://$MYBUCKET.s3.amazonaws.com/rob-iam/index.html
````

4. Task - Create a pipeline that uses Amazon S3 as a deployment provider

reference: [Tutorial](https://docs.aws.amazon.com/codepipeline/latest/userguide/tutorials-s3deploy.html)
