<!-- note marker start -->
**NOTE**: This repo contains only the documentation for the private BoltsOps Pro repo code.
Original file: https://github.com/boltopspro/infra-aws/blob/master/vendor/modules/vpc/examples/manage-default-vpc/README.md
The docs are publish so they are available for interested customers.
For access to the source code, you must be a paying BoltOps Pro subscriber.
If are interested, you can contact us at contact@boltops.com or https://www.boltops.com

<!-- note marker end -->

# Manage Default VPC

Configuration in this directory does not create new VPC resources, but it adopts [Default VPC](https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/default-vpc.html) created by AWS to allow management of it using Terraform.

This is not usual type of resource in Terraform, so use it carefully. More information is [here](https://www.terraform.io/docs/providers/aws/r/default_vpc.html).

## Usage

To run this example you need to execute:

```bash
$ terraform init
$ terraform plan
$ terraform apply
```

Run `terraform destroy` when you don't need these resources.

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
| default\_vpc\_cidr\_block | The CIDR block of the VPC |
| default\_vpc\_id | The ID of the Default VPC |

<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
