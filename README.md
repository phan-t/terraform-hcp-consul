# HCP Consul Demo with EKS

**Build time is ~15 minutes**

## How to use this module

### Post Deployment
#### Create `kubeconfig` for Amazon EKS
```shell
aws eks --region $(terraform output -raw aws_region) update-kubeconfig --name $(terraform output -raw deployment_id)
```
#### Retrieve Consul root token
```shell
terraform output consul_root_token
```