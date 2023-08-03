# camundayaml

Apply Configurations:
Run the following commands to apply the configurations:

sh
Copy code
kubectl apply -f nodeport-services.yaml
kubectl apply -f nodeport-ingress.yaml
Access Pods:
Find the external IP address of your Ingress controller using kubectl get svc -n <namespace>. Then, based on the NodePort you've configured for each service, you can access the components as follows:

Identity: http://<Ingress-Controller-IP>:<Identity-NodePort>/auth/realms/camunda-platform
Operate, Optimize, Tasklist: Similar format as above
Remember, this setup is not recommended for production and is intended for testing purposes. For a production setup, using proper DNS and LoadBalancer configurations with an Ingress controller would be more appropriate.
