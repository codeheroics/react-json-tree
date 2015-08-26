# react-json-tree

React JSON Viewer Component, Extracted from [redux-devtools](https://github.com/gaearon/redux-devtools). Supports [iterable](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Iteration_protocols#iterable) objects, such as [Immutable.js](https://facebook.github.io/immutable-js/).

![](https://img.shields.io/npm/v/react-json-tree.svg)

### Usage

```js
import JSONTree from 'react-json-tree'
import { Map } from 'immutable'

// Inside a React component:
const json = {
  array: [1, 2, 3],
  bool: true,
  object: {
    foo: 'bar'
  }  
  immutable: Map({ key: 'value' })
}

<JSONTree data={ json } />
```

#### Result:

![](http://cl.ly/image/3f2C2k2t3D0o/screenshot%202015-08-26%20at%2010.24.12%20AM.png)

Check out [examples](examples) directory for more details.

### Theming

You can pass a `theme` prop containing [base16](http://chriskempson.github.io/base16) theme data to change the theme. [The example theme data can be found here](https://github.com/gaearon/redux-devtools/tree/75322b15ee7ba03fddf10ac3399881e302848874/src/react/themes).

(The theme data is also used by [redux-devtools](https://github.com/gaearon/redux-devtools), and extracting it to a separate npm package is a TODO).

```js
const theme = {
  scheme: 'monokai',
  author: 'wimer hazenberg (http://www.monokai.nl)',
  base00: '#272822',
  base01: '#383830',
  base02: '#49483e',
  base03: '#75715e',
  base04: '#a59f85',
  base05: '#f8f8f2',
  base06: '#f5f4f1',
  base07: '#f9f8f5',
  base08: '#f92672',
  base09: '#fd971f',
  base0A: '#f4bf75',
  base0B: '#a6e22e',
  base0C: '#a1efe4',
  base0D: '#66d9ef',
  base0E: '#ae81ff',
  base0F: '#cc6633'
};

<JSONTree data={ data } theme={ theme } />
```

#### Result (Monokai Theme):

![](http://cl.ly/image/2N0a0Z2R3B0z/screenshot%202015-08-26%20at%2010.28.40%20AM.png)

### Credits

- All credits to [Dave Vedder](http://www.eskimospy.com/) ([veddermatic@gmail.com](mailto:veddermatic@gmail.com)), who wrote the original code as [JSONViewer](https://bitbucket.org/davevedder/react-json-viewer/).
- Extracted from [redux-devtools](https://github.com/gaearon/redux-devtools), which contained ES6 + inline style port of [JSONViewer](https://bitbucket.org/davevedder/react-json-viewer/) by [Daniele Zannotti](http://www.github.com/dzannotti) ([dzannotti@me.com](mailto:dzannotti@me.com))
- [Iterable support](https://github.com/gaearon/redux-devtools/pull/79) thanks to [Daniel K](https://github.com/FredyC).
- npm package created by [Shu Uesugi](http://github.com/chibicode) ([shu@chibicode.com](mailto:shu@chibicode.com)) per [this issue](https://github.com/gaearon/redux-devtools/issues/85).

### License

MIT