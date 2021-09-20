# Kubernetes

This page contains all useful information about Kubernetes.

## Resource Types
- Cronjobs 
- Deployment 
- Ingress 
- Jobs
- Node
- Pods
- Service (svc)
- Statefulsets

## Common commands
```
- Get information about the Cluster
** kubectl cluster-info

- List all resources of a kind
** kubectl get <resource_type>

- List all resources of a kind that their name matches the search string
** kubectl get <resource_type> | grep <search_string>

- Describe a resource
** kubectl describe <resource_type> <resource_name>

- Get all resource logs
** kubectl logs <resource_name>

- Get all resource logs that match the search string
** kubectl logs <resource_name> | grep 'any value'

- Delete a resource
** kubectl delete <resource_type>  <resource_name>

- Scale up/down a deployment
** kubectl scale --replicas=<desired_replicas_count> deployment <deployment_name>

- Make a resource accessible through localhost when aiming a specific port
** kubectl port-forward <resource_name> 8080:8080

- Change your current context to a specific namespace to avoid entering -n <namespace> in all commands
** kubectl config set-context --current --namespace=<namespace_name>

- When using minikube, aim your docker env to it to push new images and make them available for pods creation
** eval $(minikube docker-env)
```
**PS: You can add to most of the above commands `-n <namespace_name>` to access a specific cluster namespace or `--all-namespaces` to access all of them at once.**