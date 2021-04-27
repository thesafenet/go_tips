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

