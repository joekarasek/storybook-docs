## Issue

Running `yarn storybook` generates the following error

<details>
  <summary>Show Terminal Output</summary>
```
Built at: 06/23/2020 10:02:58 AM
                                          Asset       Size        Chunks                                Chunk Names
                            asset-manifest.json  640 bytes                [emitted]
                                    iframe.html   2.87 KiB                [emitted]
            main.19fd905cdc50a5eff581.bundle.js   20.2 KiB          main  [emitted] [immutable]         main
        main.19fd905cdc50a5eff581.bundle.js.map   9.11 KiB          main  [emitted] [dev]               main
    runtime~main.19fd905cdc50a5eff581.bundle.js   33.5 KiB  runtime~main  [emitted] [immutable]         runtime~main
runtime~main.19fd905cdc50a5eff581.bundle.js.map   34.7 KiB  runtime~main  [emitted] [dev]               runtime~main
    vendors~main.19fd905cdc50a5eff581.bundle.js   6.62 MiB  vendors~main  [emitted] [immutable]  [big]  vendors~main
vendors~main.19fd905cdc50a5eff581.bundle.js.map   6.88 MiB  vendors~main  [emitted] [dev]               vendors~main
Entrypoint main [big] = runtime~main.19fd905cdc50a5eff581.bundle.js runtime~main.19fd905cdc50a5eff581.bundle.js.map vendors~main.19fd905cdc50a5eff581.bundle.js vendors~main.19fd905cdc50a5eff581.bundle.js.map main.19fd905cdc50a5eff581.bundle.js main.19fd905cdc50a5eff581.bundle.js.map
[0] multi ./node_modules/@storybook/core/dist/server/common/polyfills.js ./node_modules/@storybook/core/dist/server/preview/globals.js ./node_modules/@storybook/addon-docs/dist/frameworks/common/config.js ./node_modules/@storybook/addon-docs/dist/frameworks/react/config.js ./.storybook/generated-entry.js ./node_modules/webpack-hot-middleware/client.js?reload=true&quiet=true 88 bytes {main} [built]
[./.storybook/generated-entry.js] 336 bytes {main} [built]
[./node_modules/@storybook/addon-docs/blocks.js] 43 bytes {vendors~main} [built]
[./node_modules/@storybook/addon-docs/dist/frameworks/common/config.js] 292 bytes {vendors~main} [built]
[./node_modules/@storybook/addon-docs/dist/frameworks/react/config.js] 672 bytes {vendors~main} [built]
[./node_modules/@storybook/addon-docs/dist/frameworks/react/extractProps.js] 2.21 KiB {vendors~main} [built]
[./node_modules/@storybook/addon-docs/dist/lib/docgen/index.js] 932 bytes {vendors~main} [built]
[./node_modules/@storybook/client-api/dist/index.js] 3.82 KiB {vendors~main} [built]
[./node_modules/@storybook/core/dist/server/common/polyfills.js] 120 bytes {vendors~main} [built]
[./node_modules/@storybook/core/dist/server/preview/globals.js] 93 bytes {vendors~main} [built]
[./node_modules/@storybook/core/node_modules/webpack/buildin/harmony-module.js] (webpack)/buildin/harmony-module.js 573 bytes {vendors~main} [built]
[./node_modules/@storybook/core/node_modules/webpack/buildin/module.js] (webpack)/buildin/module.js 497 bytes {vendors~main} [built]
[./node_modules/@storybook/react/dist/client/index.js] 1.34 KiB {vendors~main} [built]
[./node_modules/airbnb-js-shims/index.js] 40 bytes {vendors~main} [built]
[./node_modules/webpack-hot-middleware/client.js?reload=true&quiet=true] 7.68 KiB {vendors~main} [built]
    + 1353 hidden modules

WARNING in ./src/stories/2-markdown.mdx
Module build failed (from ./node_modules/babel-loader/lib/index.js):
SyntaxError: /Users/karasek/code/storybook-sandbox/src/stories/2-markdown.mdx: Unexpected token (10:9)

   8 | const makeShortcode = name => function MDXDefaultShortcode(props) {
   9 |   console.warn("Component " + name + " was not imported, exported, or provided by MDXProvider as global scope")
> 10 |   return <div {...props}/>
     |          ^
  11 | };
  12 |
  13 | const layoutProps = {
    at Parser._raise (/Users/karasek/code/storybook-sandbox/node_modules/@babel/parser/lib/index.js:742:17)
    at Parser.raiseWithData (/Users/karasek/code/storybook-sandbox/node_modules/@babel/parser/lib/index.js:735:17)
    at Parser.raise (/Users/karasek/code/storybook-sandbox/node_modules/@babel/parser/lib/index.js:729:17)
    at Parser.unexpected (/Users/karasek/code/storybook-sandbox/node_modules/@babel/parser/lib/index.js:8752:16)
    at Parser.parseExprAtom (/Users/karasek/code/storybook-sandbox/node_modules/@babel/parser/lib/index.js:10047:20)
    at Parser.parseExprSubscripts (/Users/karasek/code/storybook-sandbox/node_modules/@babel/parser/lib/index.js:9597:23)
    at Parser.parseMaybeUnary (/Users/karasek/code/storybook-sandbox/node_modules/@babel/parser/lib/index.js:9577:21)
    at Parser.parseExprOps (/Users/karasek/code/storybook-sandbox/node_modules/@babel/parser/lib/index.js:9447:23)
    at Parser.parseMaybeConditional (/Users/karasek/code/storybook-sandbox/node_modules/@babel/parser/lib/index.js:9420:23)
    at Parser.parseMaybeAssign (/Users/karasek/code/storybook-sandbox/node_modules/@babel/parser/lib/index.js:9375:21)
    at Parser.parseExpression (/Users/karasek/code/storybook-sandbox/node_modules/@babel/parser/lib/index.js:9327:23)
    at Parser.parseReturnStatement (/Users/karasek/code/storybook-sandbox/node_modules/@babel/parser/lib/index.js:11443:28)
    at Parser.parseStatementContent (/Users/karasek/code/storybook-sandbox/node_modules/@babel/parser/lib/index.js:11124:21)
    at Parser.parseStatement (/Users/karasek/code/storybook-sandbox/node_modules/@babel/parser/lib/index.js:11076:17)
    at Parser.parseBlockOrModuleBlockBody (/Users/karasek/code/storybook-sandbox/node_modules/@babel/parser/lib/index.js:11650:25)
    at Parser.parseBlockBody (/Users/karasek/code/storybook-sandbox/node_modules/@babel/parser/lib/index.js:11637:10)
 @ \.)(?=.)[^/]*?\.mdx\/?)$ (./src sync ^\.\/(?:(?:(?!\.)(?:(?:(?!(?:|\/)\.).)*?)\/)?(?!\.)(?=.)[^/]*?\.mdx\/?)$) ./stories/2-markdown.mdx
 @ ./.storybook/generated-entry.js
 @ multi ./node_modules/@storybook/core/dist/server/common/polyfills.js ./node_modules/@storybook/core/dist/server/preview/globals.js ./node_modules/@storybook/addon-docs/dist/frameworks/common/config.js ./node_modules/@storybook/addon-docs/dist/frameworks/react/config.js ./.storybook/generated-entry.js ./node_modules/webpack-hot-middleware/client.js?reload=true&quiet=true
Child HtmlWebpackCompiler:
                          Asset      Size               Chunks  Chunk Names
    __child-HtmlWebpackPlugin_0  6.47 KiB  HtmlWebpackPlugin_0  HtmlWebpackPlugin_0
    Entrypoint HtmlWebpackPlugin_0 = __child-HtmlWebpackPlugin_0
    [./node_modules/@storybook/core/node_modules/html-webpack-plugin/lib/loader.js!./node_modules/@storybook/core/dist/server/templates/index.ejs] 2.13 KiB {HtmlWebpackPlugin_0} [built]
```
</details>
