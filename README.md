# gRPC Demonstration

This project is for practice and study the grpc and protocol buffer technologies.

## Requirements

- [Golang](https://go.dev/doc/install)
- [Sqlite3](https://www.sqlite.org/draft/download.html)
- [Evans](https://github.com/ktr0731/evans)
- [Protoc](https://grpc.io/docs/protoc-installation/)

## How to start

1. Firstly, you need to install the dependencies

```
$ go mod tidy
```

2. So, you must create the database

```
$ sqlite3
$ create table categories(id string, name string, description string);
```

3. After that, you need to run the application

```
$ go run cmd/grpc-server/main.go
```

4. Now we have the server up and we can to execute the evans, evans is a gRpc client

```
$ evans -r repl
$ package pb
$ service CategoryService
// Now you can call what service you want (You can check out the options in proto/course_category.proto)
$ call CreateCategory  // It will prompt you some questions
```
