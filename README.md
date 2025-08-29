# Assignment 6 – Event-Driven Data Pipeline (AWS + Terraform)


## What this does
- Collects user-activity events via a Lambda (Python).
- Stores raw events in S3.
- Orchestrates processing with Step Functions.
- Validates, transforms, and persists processed records to DynamoDB.
- Monitors pipeline health with CloudWatch alarms (Lambda Errors, Step Functions ExecutionsFailed).
- **All infrastructure provisioned with Terraform** (no console).


## Prereqs
- Terraform >= 1.6
- Python 3.10+
- AWS CLI v2 configured (`aws configure`) with a role/user that can create the listed resources.


## Deploy
```bash
cd terraform
terraform init
terraform apply -auto-approve
