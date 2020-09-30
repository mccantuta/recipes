# Google Cloud Platform recipes

## Compute Engine

Create a default instance on GCE
```
gcloud compute instances create --project <PROJECT_ID> --zone <ZONE> <INSTANCE_NAME>
```

Connect by ssh to Compute Engine instance
```
gcloud compute ssh --project <PROJECT_ID> --zone <ZONE> <INSTANCE_NAME>
```

## Google Kubernates Engine

Create GKE cluster
```
gcloud container clusters create [CLUSTER-NAME]
```

Get authentication credentials for the cluster
```
gcloud container clusters get-credentials [CLUSTER-NAME]
```

Deploying an application to the cluster
```
kubectl create deployment hello-server --image=gcr.io/google-samples/hello-app:1.0
```

Expose application to external traffic
```
kubectl expose deployment hello-server --type=LoadBalancer --port 8080
```

Delete a cluster
```
gcloud container clusters delete [CLUSTER-NAME]
```
