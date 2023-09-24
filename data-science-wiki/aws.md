# AWS 💻📟☁️
### Created by @jl33-ai 👦🏻

AWS (Amazon Web Services) is a collection of cloud-based services provided by Amazon, enabling businesses to scale and improve without investing in physical infrastructure. 📈💱🏢

## Content 📚

1. [EC2 (Elastic Compute Cloud)](#ec2)
2. [S3 (Simple Storage Service)](#s3)
3. [IAM (Identity and Access Management)](#iam)
4. [RDS (Relational Database Service)](#rds)
5. [DynamoDB](#dynamodb)

<div id='ec2'>

## 🖥️ EC2 (Elastic Compute Cloud) 💻

- EC2 is a web service providing businesses with scalable compute capacity in the AWS cloud. 
- Using EC2, businesses can develop and deploy applications faster. 
- It can be integrated with most AWS services like Amazon S3, RDS, DynamoDB, etc.

```python
import boto3
ec2 = boto3.resource('ec2')

# create a new EC2 instance
instances = ec2.create_instances(
    ImageId='ami-0c55b159cbfafe1f0',
    MinCount=1,
    MaxCount=1,
    InstanceType='t2.micro',
    KeyName='ec2-keypair'
)
```
</div>

<div id='s3'>

## 📦 S3 (Simple Storage Service) ☁️

- S3 is an object storage service offering scalability, data availability, security, and performance. 
- It can be used alongside other AWS services as well as third-party applications.
 
```python
s3 = boto3.client('s3')
response = s3.create_bucket(Bucket='my-bucket-jl33-ai')
```
</div>

<div id='iam'>

## 🔐 IAM (Identity and Access Management) 🛡️

- IAM lets you securely manage access to AWS services and resources.
- It helps you create and manage AWS users and groups and allows permissions for them to control access.

```python
iam = boto3.client('iam')

response = iam.create_user(
    UserName='jl33-user'
)
```
</div>

<div id='rds'>

## 💽 RDS (Relational Database Service) 💾

- Amazon RDS makes it easy to set up, operate, and scale a relational database in the cloud. 
- It provides cost-effective and resizable capacity.

```python
rds = boto3.client('rds')

response = rds.create_db_instance(
    DBInstanceIdentifier='jl33-db',
    AllocatedStorage=5,
    DBInstanceClass='db.t2.micro',
    Engine='mysql',
)
```
</div>

<div id='dynamodb'>

## 📒 DynamoDB 📖

- Amazon DynamoDB is a key-value and document database that delivers single-digit millisecond performance at any scale. 
- It's fully managed, multiregional, and handles both document and key-value data models.

```python
dynamodb = boto3.resource('dynamodb')

table = dynamodb.create_table(
    TableName='jl33-table',
    KeySchema=[
        {'AttributeName': 'id', 'KeyType': 'HASH'},
    ],
    AttributeDefinitions=[
        {'AttributeName': 'id', 'AttributeType': 'N'},
    ],
    ProvisionedThroughput={'ReadCapacityUnits': 5, 'WriteCapacityUnits': 5}
)
```
</div>

> This is a basic overview of main AWS services. You can learn more about AWS by reviewing the [AWS Documentation](https://aws.amazon.com/documentation/). 📖🔍
