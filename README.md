# hello-api

A minimal HTTP JSON API that serves a single `/hello` endpoint.

This small example runs a server on port `:8080` and responds with a JSON object:

```json
{"language":"English","translation":"Hello"}
```

## Prerequisites

- Go 1.20+ installed (the project uses the standard library only).

## Build and run

Run directly with `go run` (recommended for development):

```bash
go run ./cmd
```

Or build a binary and run it:

```bash
go build -o hello-api ./cmd
./hello-api
```

By default the server listens on `:8080`.

## Endpoint

- GET /hello

Returns a JSON payload with a language and its translation. Example:

```bash
curl -i http://localhost:8080/hello
```

Example response:

```
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

{"language":"English","translation":"Hello"}
```

## Notes

- The HTTP handler is implemented in `cmd/main.go` as `helloHandler` which writes the JSON response.
