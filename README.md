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

## Useful Links

[Getting started with Go](https://github.com/golang/go/wiki#getting-started-with-go)

[How to Write Go Code](https://golang.org/doc/code.html)
