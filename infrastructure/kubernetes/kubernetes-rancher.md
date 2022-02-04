# Rancher

- [Install/Upgrade Rancher on a Kubernetes Cluster](https://rancher.com/docs/rancher/v2.6/en/installation/install-rancher-on-k8s/)
- [cert-manager - Failed to install " failed post-install: timed out waiting for the condition"](https://github.com/cert-manager/cert-manager/issues/4646)

```
- Seeing this with v1.5.1 as well. I had to clean up resources manually and then the install worked with these flags:
```
helm uninstall cert-manager -n cert-manager
kubectl delete roles cert-manager-startupapicheck:create-cert -n cert-manager;
kubectl delete serviceaccount cert-manager-startupapicheck -n cert-manager;
kubectl delete serviceaccount default -n cert-manager;
kubectl delete jobs cert-manager-startupapicheck -n cert-manager;
kubectl delete rolebindings cert-manager-startupapicheck:create-cert -n cert-manager;
Finally:
helm install cert-manager jetstack/cert-manager --namespace cert-manager --create-namespace --version v1.5.1 --set startupapicheck.timeout=5m --set installCRDs=true
```
- [Registering a Cluster](https://rancher.com/docs/rancher/v2.5/en/cluster-provisioning/registered-clusters/)