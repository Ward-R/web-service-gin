# web-service-gin

This is my first gin/go project following a tutorial from the go.dev website. This is a RESTful API with go and gin. This is an API server with two endpoints containing a local repository of data about vintage jazz records.

https://go.dev/doc/tutorial/web-service-gin
![web-service-gin-pic](https://github.com/user-attachments/assets/933b0d2b-b066-49bc-a952-43b4cf84b8fc)

<br>

## Built With
- [Go](https://go.dev/) - Backend
- [Gin](https://gin-gonic.com/) - Front-end Gin/Go

## Use

Open a command prompt and change to your home directory.

# On Linux or Mac:
```
$ cd
```
# Windows:
```
C:\> cd %HOMEPATH%
```
Using the command prompt, create a directory for your code called web-service-gin.
```
$ mkdir web-service-gin
$ cd web-service-gin
```
# Create a module in which you can manage dependencies.

Run the go mod init command, giving it the path of the module your code will be in.
```
$ go mod init example/web-service-gin
go: creating new go.mod: module example/web-service-gin
```
Run the code¶

# Begin tracking the Gin module as a dependency.

At the command line, use go get to add the github.com/gin-gonic/gin module as a dependency for your module. Use a dot argument to mean “get dependencies for code in the current directory.”
```
$ go get .
go get: added github.com/gin-gonic/gin v1.7.2
```
Go resolved and downloaded this dependency to satisfy the import declaration you added in the previous step.

From the command line in the directory containing main.go, run the code. Use a dot argument to mean “run code in the current directory.”
```
$ go run .
```
Once the code is running, you have a running HTTP server to which you can send requests.

# GET /albums
```
$ curl http://localhost:8080/albums \
    --header "Content-Type: application/json" \
    --request "GET"
```
# POST /albums
```
$ curl http://localhost:8080/albums \
    --include \
    --header "Content-Type: application/json" \
    --request "POST" \
    --data '{"id": "4","title": "The Modern Sound of Betty Carter","artist": "Betty Carter","price": 49.99}'
```
# GET /albums/:id
```
$ curl http://localhost:8080/albums/2
```
## Acknowledgements
I followed the above mentioned tutorial to make this API, so it is not original work. The purpose was to further my knowledge in the Go language and Gin framework.

