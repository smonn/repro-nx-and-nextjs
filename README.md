Reproducing issues with Nx and Next.js v13.0.1+

Build fails.

Related:

- https://github.com/vercel/next.js/pull/42106
- https://github.com/nrwl/nx/issues/12912
- https://github.com/nrwl/nx/issues/12916

```sh
$ nx build web-app --verbose

> nx run web-app:build:production

info  - Skipping linting
info  - Checking validity of types
info  - Creating an optimized production build .
 >  NX   Cannot read properties of undefined (reading 'and')


TypeError: Cannot read properties of undefined (reading 'and')
    at webpack (~/nx-with-nextjs/node_modules/@nrwl/next/plugins/with-nx.js:53:64)
    at Object.config.webpack (~/nx-with-nextjs/node_modules/@nrwl/next/src/utils/config.js:60:163)
    at Object.getBaseWebpackConfig [as default] (~/nx-with-nextjs/node_modules/next/dist/build/webpack-config.js:1402:32)
    at async Promise.all (index 0)
    at async Span.traceAsyncFn (~/nx-with-nextjs/node_modules/next/dist/trace/trace.js:79:20)
    at async ~/nx-with-nextjs/node_modules/next/dist/build/index.js:448:33
    at async ~/nx-with-nextjs/node_modules/next/dist/build/index.js:433:13
    at async Span.traceAsyncFn (~/nx-with-nextjs/node_modules/next/dist/trace/trace.js:79:20)
    at async build (~/nx-with-nextjs/node_modules/next/dist/build/index.js:64:29)

 ——————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————

 >  NX   Running target "web-app:build" failed

   Failed tasks:

   - web-app:build:production

   Hint: run the command with --verbose for more details.
```
