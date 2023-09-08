Documenting all AWS CLI commands and examples would be an extensive task, as AWS offers a vast array of services, each with its own set of commands and options. However, I can provide you with a list of common AWS CLI commands and examples for some popular AWS services. Please note that AWS services and CLI commands may change over time, so it's essential to refer to the official AWS documentation for the most up-to-date information.

### AWS CLI Installation and Configuration

1. **Installing the AWS CLI**
   
   ```
   $ pip install awscli
   ```

2. **Configuring AWS CLI**

   ```
   $ aws configure
   ```

   You'll be prompted to enter your AWS Access Key ID, Secret Access Key, default region, and output format.

### S3 (Amazon Simple Storage Service)

3. **Create a Bucket**

   ```
   $ aws s3 mb s3://bucket-name
   ```

4. **List Buckets**

   ```
   $ aws s3 ls
   ```

5. **Upload a File**

   ```
   $ aws s3 cp local-file.txt s3://bucket-name/
   ```

6. **Download a File**

   ```
   $ aws s3 cp s3://bucket-name/remote-file.txt local-file.txt
   ```

### EC2 (Amazon Elastic Compute Cloud)

7. **Launch an EC2 Instance**

   ```
   $ aws ec2 run-instances --image-id ami-12345678 --instance-type t2.micro --key-name my-key-pair
   ```

8. **List EC2 Instances**

   ```
   $ aws ec2 describe-instances
   ```

9. **Stop an EC2 Instance**

   ```
   $ aws ec2 stop-instances --instance-ids i-12345678
   ```

### RDS (Amazon Relational Database Service)

10. **Create an RDS DB Instance**

    ```
    $ aws rds create-db-instance --db-instance-identifier mydbinstance --db-instance-class db.t2.micro --engine MySQL --allocated-storage 20 --master-username myuser --master-user-password mypassword
    ```

11. **List RDS DB Instances**

    ```
    $ aws rds describe-db-instances
    ```

12. **Delete an RDS DB Instance**

    ```
    $ aws rds delete-db-instance --db-instance-identifier mydbinstance --skip-final-snapshot
    ```

### Lambda (AWS Lambda)

13. **Create a Lambda Function**

    ```
    $ aws lambda create-function --function-name my-function --runtime nodejs14.x --role arn:aws:iam::123456789012:role/lambda-role --handler index.handler --code S3Bucket=my-bucket,S3Key=my-code.zip
    ```

14. **List Lambda Functions**

    ```
    $ aws lambda list-functions
    ```

15. **Invoke a Lambda Function**

    ```
    $ aws lambda invoke --function-name my-function --invocation-type RequestResponse --payload '{"key": "value"}' output.txt
    ```

These are just a few examples of AWS CLI commands for some commonly used AWS services. AWS CLI supports many more services and operations, so you should consult the AWS documentation for specific commands and options related to the services you are using.
