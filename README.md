# GoJourney
My journey of learning Go

## GOPATH

The `GOPATH` environment variable specifies the location of your workspace. If no `GOPATH` is set, it is assumed to be `$HOME/go` on Unix systems and `%USERPROFILE%\go` on Windows. If you want to use a custom location as your workspace, you can [set the `GOPATH` environment variable](https://github.com/golang/go/wiki/SettingGOPATH).

## Go Commands

```console
# build - compile packages and dependencies
go build xyz.go
./xyz
```

```console
# install - compile and install packages and dependencies
# install the compiled executable to $GOBIN
go install xyz.go
xyz
```

```console
# run - compile and run Go program
go run xyz.go
```

## Style

### Naming Convention

The visibility of a name outside a package is determined by whether its first character is upper case.

```go
SomeFunction // exported, visible to public
someFunction // unexported, visible within this package only
```

### Formatting

gofmt (reformat) all package sources inside some directory

`go fmt <directory>/...`

## Basics

### Variables

```go
var a = "initial"
// var declares 1 or more variables.

var b, c int = 1, 2
// You can declare multiple variables at once.

var d = true
// Go will infer the type of initialized variables.

var e int
// Variables declared without a corresponding initialization are zero-valued.

f := "short"
// equivalent to var f string = "short"
// The := syntax is shorthand for declaring and initializing a variable.
```

## Useful Links

* [Getting started with Go](https://github.com/golang/go/wiki#getting-started-with-go)
* [How to Write Go Code](https://golang.org/doc/code.html)
