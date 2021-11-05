# skaffold with googlecloud

=> create new project in gclud`
=> enable _Kubernetes Engine API_ under _kubernates engine / klusters_
=> create _kluster_ with _static_ version
=> install _google cloud sdk_ <d$ gcloud> <!-- to create context and connect the cluster to the cloud -->
=> <gcloud auth login> || <gcloud auth application-default login>
=> initialize gcloud <d$ gcloud init>
=> installing gcloud context <d$ gcloud container clusters get-credentials <cluster\*name>>
=> enable _Cloud Build API_ in project:cloud.google.com
=> update _skaffold.yaml_

- add `googleCloudBuild: projectId: gcloud_project_id` to _build_
- replace artifacts image _dockerUserName_ with `us.gcr.io/projectId`

=> install _namespace:ingress-nginx_ from https://kubernetes.github.io/ingress-nginx/
=> add gcloud project _load balancer ip_ to _/etc/hosts_
