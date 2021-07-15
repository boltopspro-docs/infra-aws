<!-- note marker start -->
**NOTE**: This repo contains only the documentation for the private BoltsOps Pro repo code.
Original file: https://github.com/boltopspro/infra-aws/blob/master/vendor/modules/eks/docs/enable-docker-bridge-network.md
The docs are publish so they are available for interested customers.
For access to the source code, you must be a paying BoltOps Pro subscriber.
If are interested, you can contact us at contact@boltops.com or https://www.boltops.com

<!-- note marker end -->

# Enable Docker Bridge Network

The latest versions of the AWS EKS-optimized AMI disable the docker bridge network by default. To enable it, add the `bootstrap_extra_args` parameter to your worker group template.

```hcl
locals {
  worker_groups = [
    {
      # Other parameters omitted for brevity
      bootstrap_extra_args = "--enable-docker-bridge true"
    }
  ]
}
```

Examples of when this would be necessary are:

- You are running Continuous Integration in K8s, and building docker images by either mounting the docker sock as a volume or using docker in docker. Without the bridge enabled, internal routing from the inner container can't reach the outside world.

## See More

- [Docker in Docker no longer works without docker0 bridge](https://github.com/awslabs/amazon-eks-ami/issues/183)
- [Add enable-docker-bridge bootstrap argument](https://github.com/awslabs/amazon-eks-ami/pull/187)
