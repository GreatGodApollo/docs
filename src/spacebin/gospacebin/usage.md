# Usage

To get started with gospacebin, just import it into your project:
```go
import "github.com/GreatGodApollo/gospacebin"
```

Proceeding to construct and use a spacebin client is also super easy:

```go
// The single argument is the API instance
spacebin := gospacebin.NewClient("https://api.spaceb.in")

// Do something with the client ie:

// The single argument is the content of the document
opts := gospacebin.NewCreateDocOpts("test")
doc, err := spacebin.CreateDocument(opts)
// etc, etc...
```

For more technical documentation, please look at [pkg.go.dev][godev]

[godev]: https://pkg.go.dev/github.com/GreatGodApollo/gospacebin