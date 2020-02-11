# shebang loader for webpack

## Installation

`npm install shebang-loader`

## Usage

``` javascript
var command = require("shebang!../bin/command");
// ignores the #!/bin/user/env line inside the command file.
```

In webpack.config.js
``` javascript
module: {
  rules: [
    {
      test: path.resolve(__dirname, 'node_modules/jsonstream/index.js'),
      use: 'shebang-loader',
    },
  ],
},
```

In Quasar
``` javascript
extendWebpack(cfg) {
  cfg.module.rules.push({
    test: /node_modules\/mqtt\/mqtt\.js$/,
    loader: "shebang",
  })
},
},
```

## License

MIT (http://www.opensource.org/licenses/mit-license.php)
