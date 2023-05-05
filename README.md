# Grid-and-Cloud
To get this working:
1. Put 4 YAML files and nginx.conf in the same folder
2. Open terminal (command line, bash, shell, your choice) in this same folder
3. Write these commands:
- `kubectl apply -f backend-deployment.yaml`
- `kubectl apply -f backend-service.yaml`
- `kubectl apply -f frontend-deployment.yaml`
- `kubectl apply -f frontend-service.yaml`
4. To get ip also write `kubectl get service frontend-service --watch` command
It will output some info about frontend service, there will be EXTERNAL-IP column. In this column there is ip you need
(although it's probably would be localhost)
5. Send request on this ip (I tried it with Postman app, sent there basic get-request)
