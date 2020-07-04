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

