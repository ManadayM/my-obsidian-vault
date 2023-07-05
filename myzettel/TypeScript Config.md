---
template: note
aliases: [TS Config, tsconfig.json]
last_reviewed: "2022-12-31"
---
![tp.web.random_picture](https://images.unsplash.com/photo-1476514525535-07fb3b4ae5f1?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYyMDQ1MTc1&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-09-01) | (time:: 20:42) | (weather:: Vadodara: ☀️   +32°C ←4km/h)

# tsconfig.json
- The `tsconfig.json` file is used to change the [[TypeScript]] compiler options and settings.
- To generate `tsconfig.json` run the following command.
```shell
tsc --init
```

## Watch mode
Use the flag `-w` to start the TypeScript compiler in watch mode. TypeScript will recompile everything when it detects any change inside the source files (`rootDir`).

```shell
tsc -w
```

## Key Compiler Options
#### `outDir`
The relative path where we want to place our compiled code. Generally, it is a `build` or `dist` directory in our project.
#### `rootDir`
Relative path reference that holds our source code. Generally, it is `src` directory in our project.

---
#### Internal Links
[[2022-09-01]], [[TypeScript]]