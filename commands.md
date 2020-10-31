## Docker 
Levantar un servicio
```
    docker-compose up -d redis
```

Levantar todos los servicios
```
    docker-compose up -d
```

Listar los contenedores
```
    docker ps
    docker-compose ps 
```

Ver los logs de un servicio
```
    docker-compose logs -f web
```

Escalar un servicio
```
    docker-compose scale web=2
```

Bajar un servicio
```
    docker-compose down
```

## Docker swarm

```
docker swarm init
docker stack deploy mystackname --compose-file docker-compose.yml
```

En caso de no levantar postgres ir a la carpeta `/apps/postgres` y correr
```
docker build . -t postgres:safe
```
Despues volver a correr los comandos de kubernetes


## Kubernetes

Listar todo
```
kubectl get all
```

Desplegar de manera declarativa
```
kubectl apply -f deployment.yml
```

Obtener listado de objetos
```
kubectl get pods
kubectl get deployments
```

Listar logs de la app
```
kubectl logs --selector name=brounder -f --prefix
```

Remover objetos
```
kubectl delete --all pods
kubectl delete --all deployments
kubectl delete --all services
kubectl delete --all secrets
```

