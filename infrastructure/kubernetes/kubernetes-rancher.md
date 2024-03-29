# Rancher

- [K3s vs K8s: The Best Kubernetes Home Lab Distribution](https://www.virtualizationhowto.com/2023/07/k3s-vs-k8s-the-best-kubernetes-home-lab-distribution/)
- [Install/Upgrade Rancher on a Kubernetes Cluster](https://rancher.com/docs/rancher/v2.6/en/installation/install-rancher-on-k8s/)
- [cert-manager - Failed to install " failed post-install: timed out waiting for the condition"](https://github.com/cert-manager/cert-manager/issues/4646)

Seeing this with v1.5.1 as well. I had to clean up resources manually and then the install worked with these flags:

```shell
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

- [Traefik Proxy 2.x and Kubernetes 101 and Dashboard](https://traefik.io/blog/traefik-proxy-kubernetes-101/)

Certificate expired:

- [Workaround - Kubernets (k3s): expired certs on cluster](https://stackoverflow.com/questions/64900515/kubernets-k3s-expired-certs-on-cluster)
- [Fix - Expired K3s certificates are not automatically rotated causing connection issues](https://www.ibm.com/support/pages/expired-k3s-certificates-are-not-automatically-rotated-causing-connection-issues) 
