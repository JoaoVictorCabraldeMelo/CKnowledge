Como rodar 
```
docker run --name postgres -p 5432:5432 -v /tmp/database:/var/lib/postgresql/data -e POSTGRES_PASSWORD=123123 -d postgres
```

