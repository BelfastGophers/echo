# echo
echo program used during our first Golang workshop. The `hello_world` branch
contains a simple hello world app where as the `cli_args` branch extends the 
app to accept the message as an argument and then print it. 

This repository is intended as a reference solution for participants.


# hello world
This version of the echo program simply prints the traditional 'hello world'
message to the screen. It uses the [fmt][1] package in particular the [Println][2]
function.

To run this code, clone the repo and use `go build` to build the program and
execute it with `./echo`.


[1]: https://godoc.org/fmt
[2]: https://godoc.org/fmt#Println
