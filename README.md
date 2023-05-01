# Welog

![build](https://github.com/iamando/welog/workflows/build/badge.svg)
![license](https://img.shields.io/github/license/iamando/welog?color=success)
![Go version](https://img.shields.io/github/go-mod/go-version/iamando/welog)
[![GoDoc](https://godoc.org/github.com/iamando/welog?status.svg)](https://godoc.org/github.com/iamando/welog)

A simple and colorful logging module for Go. It allows developers to easily log messages at different log levels, including Debug, Info, Warn, and Error.

## Install

```bash
go get github.com/iamando/welog
```

## Usage

```go
import "github.com/iamando/welog"
```

## Example

```go
package main

import (
  welog "github.com/iamando/welog"
)


func ExampleUsage() {
 // create a new logger with info level with basic mode or use `welog.Colorful` to use colorful mode
 logger := welog.GenerateLogger(Info, welog.Basic) // welog.Colorful

 // log some messages
 logger.Error("An error occurred")
 logger.Warn("A warning occurred")
 logger.Info("An informational message")
 logger.Debug("A debug message")

 // set the logger level to debug
 logger.level = Debug

 // log some more messages
 logger.Error("Another error occurred")
 logger.Warn("Another warning occurred")
 logger.Info("Another informational message")
 logger.Debug("Another debug message")
}

func main() {
 ExampleUsage()
}
```

## Testing

```bash
go test
```

## Support

Welog is an MIT-licensed open source project. It can grow thanks to the sponsors and support.

## License

Welog is [MIT licensed](LICENSE).
