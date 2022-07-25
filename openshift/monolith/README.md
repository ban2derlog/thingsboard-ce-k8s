# GCP monolith deployment scripts

This folder containing scripts and Kubernetes resources configurations to run ThingsBoard in Monolith mode on GCP cluster.

You can find the deployment guide by the [**link**](https://thingsboard.io/docs/user-guide/install/cluster/gcp-monolith-setup/).

Before installation need to create service account in OpenShift for ThingsBoard and Cassandra (if Hybrid deployment):

oc create serviceaccount cassandra -n thingsboard
oc adm policy add-scc-to-user anyuid -z cassandra -n thingsboard

oc create serviceaccount thingsboard -n thingsboard
oc adm policy add-scc-to-user anyuid -z thingsboard -n thingsboard
