![CircleCI](https://img.shields.io/circleci/build/github/gogjango/gjango) [![Maintainability](https://api.codeclimate.com/v1/badges/33f9e187fee5dc62a4d7/maintainability)](https://codeclimate.com/github/gogjango/gjango/maintainability) [![Test Coverage](https://api.codeclimate.com/v1/badges/33f9e187fee5dc62a4d7/test_coverage)](https://codeclimate.com/github/gogjango/gjango/test_coverage) [![Go Report Card](https://goreportcard.com/badge/github.com/calvinchengx/gin-go-pg)](https://goreportcard.com/report/github.com/calvinchengx/gin-go-pg) ![GitHub](https://img.shields.io/github/license/calvinchengx/gin-go-pg)


# golang gin with go-pg orm

An example project that uses golang gin as webserver, and go-pg library for connecting with a PostgreSQL database.

## Get started

```bash
# postgresql config
cp .env.sample .env
source .env
```

```bash
# get dependencies and run
go get -v ./...
go run .
```

## Tests and coverage

```bash
go test -coverprofile c.out ./...
go tool cover -html=c.out

# or simply
./test.sh
```

## Schema migration and cli management commands

```bash
# create a new database based on config values in .env
go run . create_db

# create our database schema
go run . create_schema

# create our superadmin user, which is used to administer our API server
go run . create_superadmin

# schema migration and subcommands are available in the migrate subcommand
# go run . migrate [command]
```
