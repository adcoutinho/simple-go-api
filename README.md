# simple-go-api

Based on: 

**Endpoints:**

```
/albums

GET – Get a list of all albums, returned as idented JSON.
POST – Add a new album from request data sent as JSON.

/albums-raw

GET - Get a list of all albums, returned as raw JSON.

/albums/:id

GET – Get an album by its ID, returning the album data as JSON.
```

How to setup:

cd web-service-gin
go mod init example/web-service-gin
go get .
go run .


Examples:

```
Get all albums:
curl http://localhost:8080/albums

More explicit way to get albums:
curl http://localhost:8080/albums \
    --header "Content-Type: application/json" \
    --request "GET"

Post a new album:
curl http://localhost:8080/albums \
    --include \
    --header "Content-Type: application/json" \
    --request "POST" \
    --data '{"id": "4","title": "The Modern Sound of Betty Carter","artist": "Betty Carter","price": 49.99}'

```
