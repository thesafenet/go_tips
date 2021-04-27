### Getting started

Check your env variables
GOPATH - The GOPATH environment variable lists places to look for Go code. If the environment variable is unset, GOPATH defaults to a subdirectory named "go" in the user's home directory ($HOME/go on Unix, %USERPROFILE%\go on Windows)
GOBIN  - The directory where 'go install' will install a command.
GOROOT - The root of the go tree. 

#Go tips and cool info

### OS and ARCH (GOOS and GOARCH)

`#go tool dist list` Will list all available OSs and architectures available for compilation

How to check the arch and os the code is running

```
package main

import (
	"fmt"
	"runtime"
)

func main() {
	fmt.Println(runtime.GOOS, runtime.GOARCH)
}
```
*Output:*
```
windows amd64
```


### Testing
Create a new file with <package name>_test.go
Create a funtion called Test<function name>
Follow the sections:
	- initialization 
	- execution 
	- verification/validation
	
function example
```
funct TestExample(t *testing.T){
 //initialization
 x:=10
 
 //execution
 res := Example(x)
 
 //validation
 if res < 10 {
  t.Errorf("Expected <10 got %s",res)
 }
}
```

*Testing a funtion to take less than a certain time*


### Benchmarking
To monitor the performance
```
funct TestExample(t *testing.B){
    for i := 0; i < b.N; i++ {
        Example(i)
    }
}
```		

### Project template
https://github.com/thockin/go-build-template

### Folder structure
src 
  -<repositories>
  -github.com
    -<project>
      -cmd
        -<application>
	  -main.go
	-<anotherapp>
	  -app.go (with own pacage name 'anotherapp')
      -pkg
        -codeaslibrary
	  -library.go
	-api
	  -file.go
      -api
      -vendor
      -internal
    -project a 
    -project b
  -golang/org
  -gitlab.com
pkg
  -linux_amd64
  -libary
    -file.go
  -windows_amd64
bin 



