```docker build -t approver .```

```docker run -e API_URL=http://localhost:8090 -p 3001:3000 approver```

```docker tag approver:test yourusername/approver:test```
```docker tag approver yourusername/approver:test```

```docker login```

```docker push yourusername/approver:test```

```docker logs frappe-docker-create-site-1 -f```

```docker images```

```docker run -d --name mariadb-container -p 3307:3306 mariadb:10.6```

```docker run -d --name mariadb-container -p 3307:3306 -e MARIADB_ROOT_PASSWORD=my-secret-pw mariadb:10.6```

```mysql -h 127.0.0.1 -P 3307 -u root -p --ssl=0```
```mysql -h 127.0.0.1 -P 3307 -u root -p --skip-ssl```


```docker compose -f pwd.yml build```
```docker compose -f pwd.yml down -v```
```docker compose -f pwd.yml up -d```
