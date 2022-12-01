# A simple starter kit to get started with webpack

Based on this: https://webpack.js.org/guides/getting-started/

Simply running `npx webpack` would throw the following warning that you can avoid by providing a mode parameter `npx webpack --mode development`. Added in package.json, so you can simply run `npm run dev` or `npm run prod`:

```
npx webpack
asset main.js 132 bytes [emitted] [minimized] (name: main)
./src/index.js 289 bytes [built] [code generated]

WARNING in configuration
The 'mode' option has not been set, webpack will fallback to 'production' for this value.
Set 'mode' option to 'development' or 'production' to enable defaults for each environment.
You can also set it to 'none' to disable any default behavior. Learn more: https://webpack.js.org/configuration/mode/

webpack 5.75.0 compiled with 1 warning in 160 ms
```

More about [mode configuration](https://webpack.js.org/configuration/mode/).