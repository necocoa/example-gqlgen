```sh
go version
go version go1.21.4 darwin/arm64
```

```sh
go mod init gqlgen_tutorial
printf '// +build tools\npackage tools\nimport (_ "github.com/99designs/gqlgen"\n _ "github.com/99designs/gqlgen/graphql/introspection")' | gofmt > tools.go
go mod tidy

go run github.com/99designs/gqlgen init
go mod tidy
go run server.go
```

```
go run github.com/99designs/gqlgen generate
```
