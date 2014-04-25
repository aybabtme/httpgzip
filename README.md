# package `httpgzip`

A handler that compresses `http.ResponseWriter` if it contains the `gzip`
strings in it's `Accept-Encoding` headers.

The handler flushes data as it streams it, making it suitable for long
streams of data that should be sent regularly.

# Godoc?

[Godoc!](http://godoc.org/github.com/aybabtme/httpgzip)

# Usage

```go
h := MyHandler()
gzh := httpgzip.NewHandler(h)
log.Fatal(http.ListenAndServe(":8080", gzh))
```

That's it.

