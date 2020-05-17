# eck
Elastic Cloud on Kubernetes

### Create namespace
`kubectl create namespace elasticsearch`

### Deploy operator to newly created namespace
`kubectl apply -f https://download.elastic.co/downloads/eck/1.0.0/all-in-one.yaml -n elasticsearch`

### Deploy config
`kubectl apply - f es.yaml -n elasticsearch`

The deployment yaml includes everything to get up and running with Elasticsearch and Kibana, and assumes nginx-ingress controller.  If nginx-ingress controller isn't being used, simply remove the ingress code and configure load balancer settings as described here https://www.elastic.co/guide/en/cloud-on-k8s/current/k8s-accessing-elastic-services.html

### Filebeat
Filebeat configs are also included.  Binaries are tested and confirmed to work with ECK.

Update:
1. paths
1. include lines
1. regex pattern
1. elasticsearch host
1. elasticsearch password
