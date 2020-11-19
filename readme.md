## Learn Kubernetes By Example

### Errata:

#### Pods lesson

In the twocontainers scenario you need to run this command to actually
end up in the shell.
`kubectl exec --stdin --tty twocontainers --container shell -- /bin/bash`

By default you end up in the first container on the pod:
Validate: `kubectl exec -t twocontainers  -- ls`
--> will list out the contents of the `sise` container

#### Services lesson
You need to deploy two of the sise pod and call the service from one of them and
the service will route to the other pod. Otherwise you would just call yourself
throuhg the service, which is not working. Checkl the `/services` folder.