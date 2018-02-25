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

### Package names

The first statement in a Go source file must be `package name`, where name is the package's default name for imports.  All files in a package must use the same name.  Executable commands must always use `package main`.

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

### Slice

Slice is a special data type that wraps on top of array. Slice can represent either entire array or portion of array as needed. An array has a fixed size. A slice, on the other hand, is a dynamically-sized, flexible view into the elements of an array. Unlike array which has its own storage, slice share the same storage as of the underlying array and hence multiple slice on same array will share same memory. Slice is created using built-in function make, as shown below:

```go
s := make([]int, length, capacity)
```

Initialization:
```go
s := make([]int, 0)
// or
s := []int{}
// or
array[low : high] // a half-open range which includes the first element, but excludes the last one
```

Arrays can be created using the following syntaxes:
```go
[N]Type
[N]Type{value1, value2, ..., valueN}
[...]Type{value1, value2, ..., valueN}
```

Slices can be created using the following syntaxes:
```go
make([]Type, length, capacity)
make([]Type, length)
[]Type{}
[]Type{value1, value2, ..., valueN}
```

Diff:
* Array
  * fixed-length
  * values
* Slice
  * dynamically-length
  * references


### Panic

A `panic` typically means something went unexpectedly wrong. Mostly we use it to fail fast on errors that shouldn’t occur during normal operation, or that we aren’t prepared to handle gracefully. A common use of panic is to abort if a function returns an error value that we don’t know how to (or want to) handle.

```go
_, err := os.Create("/tmp/file")
if err != nil {
    panic(err)
}
```

## Useful Links

* [Getting started with Go](https://github.com/golang/go/wiki#getting-started-with-go)
* [How to Write Go Code](https://golang.org/doc/code.html)
