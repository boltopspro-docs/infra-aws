<!-- note marker start -->
**NOTE**: This repo contains only the documentation for the private BoltsOps Pro repo code.
Original file: https://github.com/boltopspro/infra-aws/blob/master/README.md
The docs are publish so they are available for interested customers.
For access to the source code, you must be a paying BoltOps Pro subscriber.
If are interested, you can contact us at contact@boltops.com or https://www.boltops.com

<!-- note marker end -->

# AWS Reference Architecture

This repo contains an example AWS reference architecture. It uses the [Terraspace Framework](https://terraspace.cloud/) and a combination of [OSS](https://registry.terraform.io/browse/modules?provider=aws) and [BoltOps Pro](https://www.boltops.com/pro) modules.

## Deploy

To deploy all the infrastructure stacks:

    terraspace all up

To deploy individual stacks:

    terraspace up vpc # where vpc is app/stacks/vpc

## Dev and Prod Environments

To create multiple environments like dev and prod

    TS_ENV=dev  terraspace all up # default
    TS_ENV=prod terraspace all up

## Stacks Included

The example stacks included deploys:

* VPC: Virtual Private Network
* EC2 Instance:

## Terrafile

To use more modules, add them to the [Terrafile](https://terraspace.cloud/docs/terrafile/).
