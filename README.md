# sbom-demo

## Deploy Sock-Shop Application

 ```bash
kubectl apply -f https://raw.githubusercontent.com/JosephYostos/sbom-demo/main/sock-shop.yaml
 ```

## Install Sysdig cluster scanner on single cluster

https://sysdig-docs-pr-1444.onrender.com/en/docs/installation/sysdig-secure/install-agent-components/kubernetes/install-cluster-scanner/#full-deploy-with-cluster-scanner

## Extract SBOM


 ```bash
curl --request GET \
  -H "Authorization: Bearer xxx" \
  --url 'https://eu1.app.sysdig.com/secure/vulnerability/v1beta1/sboms?assetId=sha256:c276a3cc04187ca2e291256688a44a9b5db207762d14f21091b470f9c53794e2&assetType=container-image' | jq
 ```

### resources
https://www.youtube.com/watch?v=sC9zE5pGl_Y
