## Hello World Tutorial

* https://go.dev/doc/tutorial/getting-started

### Check Version

```
$ pwd
/Users/pnguyen/Desktop/GIT/github/golang/v1.19/tutorials/hello
$ go version
go version go1.19.2 darwin/amd64
```

### Enable dependency tracking for your code

```
$ go mod init example/hello
go: creating new go.mod: module example/hello
```

### Create hello.go

```
package main

import "fmt"

func main() {
    fmt.Println("Hello, World!")
}
```

### Run hello.go

```
$ go run .
Hello, World!
```

### Call Code in an External Package

* https://pkg.go.dev

```
package main

import "fmt"

import "rsc.io/quote"

func main() {
    fmt.Println(quote.Go())
}
```


### Add new Module Requirements and Sums

Go will add the quote module as a requirement, as well as a go.sum file for use in authenticating the module. For more, see Authenticating modules in the Go Modules Reference. 

```
$ go mod tidy
go: finding module for package rsc.io/quote
go: downloading rsc.io/quote v1.5.2
go: found rsc.io/quote in rsc.io/quote v1.5.2
go: downloading rsc.io/sampler v1.3.0
go: downloading golang.org/x/text v0.0.0-20170915032832-14c0d48ead0c
```

### Run Updated Code

```
$ go run .
Don't communicate by sharing memory, share memory by communicating.
```

