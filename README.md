# vite-bug-repro

A reproduction of broken SSR with CommonJS dependencies.

`app` depends on `pkg-a-commonjs`.

SSR crashes with `ReferenceError: module is not defined` from `pkg-a-commonjs`.

Reproduction steps:
```bash
corepack enable
yarn install
yarn node app/server.mjs
open http://localhost:5173
```
