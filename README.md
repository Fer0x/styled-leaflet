# styled-leaflet

leaflet.css for [styled-components](https://styled-components.com/).

The original `leaflet.css` is pulled from [CDN](https://unpkg.com/leaflet@1.4.0/dist/leaflet.css), and parsed into styled ready format.


## Usage

```sh
npm install --save styled-leaflet
```

### styled-components v4

styled-components [createGlobalStyle documentation](https://www.styled-components.com/docs/api#createglobalstyle)

> This is just usage example

```js
// ----- index.js
import React from 'react'
import { LeafletStyles } from 'styled-leaflet'

import { App } from './app'

const Root = () => (
  <React.Fragment>
    <LeafletStyles />
    <App />
  </React.Fragment>
)
```

Also you can use `injectGlobal` API:

```js
// ----- styles/index.js
import styledLeaflet from 'styled-leaflet'
import { injectGlobal } from 'styled-components'

injectGlobal`
  ${styledLeaflet}

  // You can continue writing global styles
  body {
    padding: 0;
    background-color: black;
  }
`
```

You can also use named imports:

```js
// ES Modules
import { leafletStyles, LeafletStyles } from 'styled-leaflet'

// CommonJS
const { leafletStyles, LeafletStyles } = require('styled-leaflet')

injectGlobal` ${leafletStyles} `
<LeafletStyles />
```

## Version

__NO SEMVER!__

Why? Because X.Y numbers in `vX.Y.Z` version matches X.Y in `leaflet`

## License

The [MIT License](LICENSE.md)

