### Base 45 Encoding / Decoding in go

This library is a basic implementation of base 45 encoding defined on  [https://datatracker.ietf.org/doc/draft-faltstrom-base45/](https://datatracker.ietf.org/doc/draft-faltstrom-base45/)

### Sample usage

```go
package main

import (
	"fmt"
	"github.com/xkmsoft/base45"
	"log"
)

func main() {
	in := "Hello!!"
	encoded := base45.Encode(in)
	decoded, err := base45.Decode(encoded)
	if err != nil {
		log.Fatal(err)
	}
	fmt.Printf("Input: %s\n", in)
	fmt.Printf("Base45 Encoded: %s\n", encoded)
	fmt.Printf("Base45 Decoded: %s\n", decoded)
}
```

```
Input: Hello!!
Base45 Encoded: %69 VD92EX0
Base45 Decoded: Hello!!

```
