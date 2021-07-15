<!-- note marker start -->
**NOTE**: This repo contains only the documentation for the private BoltsOps Pro repo code.
Original file: https://github.com/boltopspro/infra-aws/blob/master/vendor/modules/rds/modules/db_parameter_group/README.md
The docs are publish so they are available for interested customers.
For access to the source code, you must be a paying BoltOps Pro subscriber.
If are interested, you can contact us at contact@boltops.com or https://www.boltops.com

<!-- note marker end -->

# aws_db_parameter_group

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Requirements

| Name | Version |
|------|---------|
| terraform | >= 0.12.6 |
| aws | >= 2.49 |

## Providers

| Name | Version |
|------|---------|
| aws | >= 2.49 |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| create | Whether to create this resource or not? | `bool` | `true` | no |
| description | The description of the DB parameter group | `string` | `""` | no |
| family | The family of the DB parameter group | `string` | n/a | yes |
| identifier | The identifier of the resource | `string` | n/a | yes |
| name | The name of the DB parameter group | `string` | `""` | no |
| name\_prefix | Creates a unique name beginning with the specified prefix | `string` | `""` | no |
| parameters | A list of DB parameter maps to apply | `list(map(string))` | `[]` | no |
| tags | A mapping of tags to assign to the resource | `map(string)` | `{}` | no |
| use\_name\_prefix | Whether to use name\_prefix or not | `bool` | `true` | no |

## Outputs

| Name | Description |
|------|-------------|
| this\_db\_parameter\_group\_arn | The ARN of the db parameter group |
| this\_db\_parameter\_group\_id | The db parameter group id |

<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
