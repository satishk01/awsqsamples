# ECS with Network Load Balancer and API Gateway Integration

This Terraform configuration creates:

1. An ECS Fargate service
2. A Network Load Balancer (NLB) to route traffic to the ECS service
3. An API Gateway HTTP API with a VPC Link to the NLB

## Architecture

```
Internet → API Gateway → VPC Link → Network Load Balancer → ECS Service
```

## Prerequisites

- AWS CLI configured with appropriate credentials
- Terraform installed (v0.14+)

## Usage

1. Initialize Terraform:
   ```
   terraform init
   ```

2. Review the plan:
   ```
   terraform plan
   ```

3. Apply the configuration:
   ```
   terraform apply
   ```

4. To destroy the resources:
   ```
   terraform destroy
   ```

## Accessing the Service

After deployment, you can access your service through:

1. The NLB endpoint directly (see output `nlb_dns_name`)
2. The API Gateway endpoint (see output `api_gateway_endpoint`)

## Customization

Modify the `variables.tf` file to customize:
- AWS region
- Container image
- Instance count
- CPU and memory allocation
- Port configurations
