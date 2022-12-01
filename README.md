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

When trying to use uglify plugin I got an error so using terser instead. Apparently uglify is not compatible to webpack 5; instead of using --force, or --legacy-peer-deps better switch to something more compatible.

```
npm ERR! code ERESOLVE
npm ERR! ERESOLVE unable to resolve dependency tree
npm ERR! 
npm ERR! While resolving: webpack-starter@1.0.0
npm ERR! Found: webpack@5.75.0
npm ERR! node_modules/webpack
npm ERR!   dev webpack@"^5.75.0" from the root project
npm ERR! 
npm ERR! Could not resolve dependency:
npm ERR! peer webpack@"^4.0.0" from uglifyjs-webpack-plugin@2.2.0
npm ERR! node_modules/uglifyjs-webpack-plugin
npm ERR!   dev uglifyjs-webpack-plugin@"*" from the root project
npm ERR! 
npm ERR! Fix the upstream dependency conflict, or retry
npm ERR! this command with --force, or --legacy-peer-deps
npm ERR! to accept an incorrect (and potentially broken) dependency resolution.

```