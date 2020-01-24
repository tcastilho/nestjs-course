```bash
$ docker run \
  --name postgres \
  -e POSTGRES_USER=postgres \
  -e POSTGRES_PASSWORD=postgres \
  -e POSTGRES_DB=taskmanagement \
  -p 5432:5432 \
  -d \
  postgres
```

```bash
$ docker ps
```

```bash
$ docker exec -it postgres /bin/bash
```

```bash
$ docker run \
  --name adminer \
  -p 8080:8080 \
  --link postgres:postgres \
  -d \
  adminer
```
