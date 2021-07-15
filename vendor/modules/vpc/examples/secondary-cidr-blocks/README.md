<!-- note marker start -->
**NOTE**: This repo contains only the documentation for the private BoltsOps Pro repo code.
Original file: https://github.com/boltopspro/infra-aws/blob/master/vendor/modules/vpc/examples/secondary-cidr-blocks/README.md
The docs are publish so they are available for interested customers.
For access to the source code, you must be a paying BoltOps Pro subscriber.
If are interested, you can contact us at contact@boltops.com or https://www.boltops.com

<!-- note marker end -->

# Simple VPC with secondary CIDR blocks

Configuration in this directory creates set of VPC resources across multiple CIDR blocks.

There is a public and private subnet created per availability zone in addition to single NAT Gateway shared between all 3 availability zones.

## Usage

To run this example you need to execute:

```bash
$ terraform init
$ terraform plan
$ terraform apply
```

Note that this example may create resources which can cost money (AWS Elastic IP, for example). Run `terraform destroy` when you don't need these resources.

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Requirements

| Name | Version |
|------|---------|
| terraform | >= 0.12.7 |
| aws | >= 2.68 |

## Providers

No provider.

## Inputs

No input.

## Outputs

| Name | Description |
|------|-------------|
| nat\_public\_ips | List of public Elastic IPs created for AWS NAT Gateway |
| private\_subnets | List of IDs of private subnets |
| public\_subnets | List of IDs of public subnets |
| vpc\_cidr\_block | The CIDR block of the VPC |
| vpc\_id | The ID of the VPC |
| vpc\_secondary\_cidr\_blocks | List of secondary CIDR blocks of the VPC |

 <!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
