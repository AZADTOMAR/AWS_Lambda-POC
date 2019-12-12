# AWS_Lambda-POC
Using python start-stop aws instances with a tag.

Create Tag on EC2 instances- Tag Key- "Type", Value- "Scheduled"
Schedule EC2 instances from Monday to Friday Start Morning 9 am and Stop Night 11 pm.

Aws Services use-

1. IAM 
2. Lambda 
3. Cloudwatch 
4. EC2 

Steps:

1. IAM Role for Lambda - EC2 instance, AWS Cloudwatch Logs
2. Creation of Lambda function in python-3.6
3. Schedule Lambda function
IST to GMT convertion 
https://www.worldtimebuddy.com/ist-to-gmt-converter

Describition: 

In our Aws account Ec2 instances should be launch then which Ec2 instance we want to automate add tag. 
then create an IAM role for lambda with policy (custom/default).I have created my own custom policy.
Now create a lambda function start_ec2 in python 3.6 with your IAM role then write lambda_function save and then test after that go to cloudwatch dashboard and Click event create a rule with schedule 
option in cron expression. Use IST To GMT conversion for your desire schedule. now target lambda fuction start_ec2/stop_ec2 then configure detail schedule.

Usages: 

Lambda is a serverless compute service. it helps us to automate our aws infrastructure tasks. Lambda along with other AWS services can be used to build a powerful website without having to manage a single server or an operating system.
Use Case- Serverless E-commerce Website which uses AWS Lambda use cases for payment management, cart management and recommendation engine.

Run Environment Limitation:
1. The disk space is limited to 512 MB. 
2. The default deployment package size is 50 MB.
3. Memory range is from 128 to 1536 MB.
4. Maximum execution timeout for a function is 15 minutes.
5. Request and response body payload size are maximized to 6 MB.
6. Event request body can be up to 128 KB.


