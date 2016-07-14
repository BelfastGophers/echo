# echo
echo program used during our first Golang workshop. The `hello_world` branch
contains a simple hello world app where as the `cli_args` branch extends the 
app to accept the message as an argument and then print it. 

This repository is intended as a reference solution for participants.


# command line arguments
This version of the echo program accepts an number of arguments from th command
line and prints them on screen.

For the program we are introducing another package, the [os][1] package from the
Go standard library. The [os][1] package provides access to operating system
functionality. For this vesion of echo we are using the [Args][2] variable, which
gives us the aruments pased to the program begining with the program name.

The next thing we introduce is the [for loop][3], Go's only loop construct. We
use the for loop to iterate through all the arguments passed to the program
using `range`. When iterating through an [array][4] using range it returns an
index and value, e.g.

```go
for index, v := array {
	...
}
```

[Slices][5] wrap arrays to give a more powerful and convenient interface. As the
first argument passed to the program is the program name we want to ignore this
and not print it. Using `[1:]` can be read as from position 1 to the end. 

In this program we are not concerned with the index so we use the blank identifier
a  `_` to ignore the value. Remember an unused variable in Go is an error.


Use `go build` to build the program and the run it passing any number of arguments

```
./echo one two three
one
two
three
```

We print each argument on a separate line to make it clear we're processing each
argument separately.

[1]: https://godoc.org/os
[2]: https://godoc.org/os#pkg-variables
[3]: https://golang.org/doc/effective_go.html#for
[4]: https://golang.org/doc/effective_go.html#arrays
[5]: https://golang.org/doc/effective_go.html#slices
