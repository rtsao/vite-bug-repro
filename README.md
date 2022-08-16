# vite-bug-repro

A reproduction of broken SSR with CommonJS sub-dependencies.

`app` depends on `pkg-c`, which depends on `pkg-b`, which depends on `pkg-a-commonjs`.

SSR crashes with `ReferenceError: module is not defined` from `pkg-a-commonjs`.

Reproduction steps:
```bash
corepack enable
yarn install
yarn node app/server.mjs
open http://localhost:5173
```
