
# Go REST Postgres

## Build

### From code
```shell script
go get -t -d -v ./...
go build -v ./...
```

### From Docker
```shell script
docker build . -t go-postgres:latest
```

---

## Run

### Preliminary steps
1. Build application
2. Spin up PostgreSQL with Docker
	```shell script
	docker run -d --name postgres \
		-e POSTGRES_PASSWORD=supersecret \
		-p 5432:5432 \
		postgres
	```

### From code
```shell script
./go-postgres
```

### From Docker
```shell script
docker run -d --name go-postgres -p 8080:8080 go-postgres:latest
```

---

## REST endpoints

- `GET /products` > Fetch a list of products in response to a valid 
- `GET /products/{id}` > Fetch a product in response to a valid 
- `POST /products` > Create a new product in response to a valid 
- `PUT /products/{id}` > Update a product in response to a valid 
- `DELETE /products/{id}` > Delete a product in response to a valid 

---

## Links
- https://semaphoreci.com/community/tutorials/building-and-testing-a-rest-api-in-go-with-gorilla-mux-and-postgresql
- https://errorsingo.com/github.com-lib-pq-err-ssl-not-supported/
