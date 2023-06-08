# Orkes-k8s
Configuration and scripts for running the Orkes Conductor proof of concept.

## PostgreSQL
* [Configuration Map with Credentials](k8s/postgres-configmap.yaml)
* [Persistent Volume Definition and Clain](k8s/postgres-pvc-pv.yaml)
* [Deployment Definition](k8s/postgres-deployment.yaml)
* [Database Service](k8s/postgres-service.yaml)

To attach to the running PostgreSQL pod use:

```shell
$ kubectl exec -it [pod-name] --  psql -h localhost -U admin --password -p 5432 postgresdb
```

## redis
* [Configuration Map with Credentials](k8s/redis-configmap.yaml)
* [Persistent Volume Definition and Clain](k8s/redis-pvc-pv.yaml)
* [Deployment Definition](k8s/redis-deployment.yaml)
* [Database Service](k8s/redis-service.yaml)

```shell
$ kubectl exec -it [pod-name] -- /bin/bash
root@redis-78dc8f4899-nrkmb:/data# redis-cli
127.0.0.1:6379> 
```

