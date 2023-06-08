# Orkes-k8s
Configuration and scripts for running the Orkes Conductor proof of concept.

## PostgreSQL
* [Configuration Map with Credentials](k8s/postgres-configmap.yaml)
* [Persistent Volume Definition and Clain](k8s/postgres-pvc-pv.yaml)
* [Deployment Definition](k8s/postgres-deployment.yaml)
* [Database Service](k8s/postgres-service.yaml)

To attach to the running PostgreSQL pod use:

```bash
$ kubectl exec -it [pod-name] --  psql -h localhost -U admin --password -p 5432 postgresdb
```