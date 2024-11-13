# Api-Golang
RESTful API server with two endpoints; a repository of data about vintage jazz records.
In this project I'll be storing the data in memory.
* Storing data in memory means that the set of albums will be lost each time you stop the server, then recreated when you start it.

### Prerequisites
* Go install for Mac
  ```sh
  curl -O https://dl.google.com/go/go1.20.5.darwin-amd64.tar.gz
  ```

* Clone the repo
   ```sh
   git clone https://github.com/Maysa87/api-golang.git
   ```
* Install Gin package
   ```sh
   go get -u github.com/gin-gonic/gin
   ```
* To make a request to the running web service and add a new album to the existing list.
   ```sh
   $ curl http://localhost:8080/albums \
    --include \
    --header "Content-Type: application/json" \
    --request "POST" \
    --data '{"id": "Number Id", "title": "tittle of the album", "artist": "artist's name", "price": 0.00}'
   ```

* Command to see all album:
   ```sh
   $ curl http://localhost:8080/albums
   ```
