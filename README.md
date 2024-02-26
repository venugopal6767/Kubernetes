# Kubernetes-Practice
kubectl run my-pod --image=my-container-image:latest --port=8080 \
--env="ENV_VAR=value" \
--labels="app=myapp,env=production" \
--annotations="description=My production pod" \
--restart=Never \
--serviceaccount=my-service-account \
--image-pull-policy=Always \
--command -- /bin/bash -c "echo Hello Kubernetes" \
--dry-run=client -o yaml > pod.yaml


in single line:
kubectl run <pod-name> --image=<container-image> --port=<container-port> --env="<key1=value1,key2=value2>" --labels="<key1=value1,key2=value2>" --annotations="<key1=value1,key2=value2>" --restart=<restart-policy> --serviceaccount=<service-account> --image-pull-policy=<pull-policy> --command -- <command-to-run> --dry-run=client -o yaml
