# latin-modern

[![GitHub release](https://img.shields.io/github/release/go-fonts/latin-modern.svg)](https://github.com/go-fonts/latin-modern/releases)
[![GoDoc](https://godoc.org/github.com/go-fonts/latin-modern?status.svg)](https://godoc.org/github.com/go-fonts/latin-modern)
[![License](https://img.shields.io/badge/License-BSD--3-blue.svg)](https://github.com/go-fonts/latin-modern/raw/master/LICENSE)

`latin-modern` provides the [Latin Modern](http://www.gust.org.pl/projects/e-foundry/latin-modern) fonts as importable Go packages.

The fonts are released under the [GUST font](https://github.com/go-fonts/latin-modern/raw/master/LICENSE-GUST) license.
The Go packages under the [BSD-3](https://github.com/go-fonts/latin-modern/raw/master/LICENSE) license.

## Example

```go
import (
	"fmt"
	"log"

	"github.com/go-fonts/latin-modern/lmmath"
	"golang.org/x/image/font/sfnt"
)

func Example() {
	ttf, err := sfnt.Parse(lmmath.TTF)
	if err != nil {
		log.Fatalf("could not parse Latin Modern Math font: %+v", err)
	}
	fmt.Printf("num glyphs: %d\n", ttf.NumGlyphs())

	// Output:
	// num glyphs: 4802
}
```
