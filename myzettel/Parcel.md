---
template: note
---
![tp.web.random_picture](https://images.unsplash.com/photo-1531171138563-f6c0692e8238?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYwMTIwMzQ1&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-08-10) | (time:: 14:02) | (weather:: Vadodara: 🌧   +28°C ↑14km/h)

# Parcel
[Getting started with Parcel](https://parceljs.org/getting-started/webapp/)
- A bundling tool popular for its **zero-configuration** philosophy.
- Emerged as a [[Webpack]] alternative.
- Built-in support for `SASS`, `JSX`, `TS`, `Image Optimization`, and much more.
- **Just point it at your project and it'll compile everything, and start up a local server for development with hot reload support.**

## Install
```shell
npm i parcel --location=global
```

## Run
```shell
npx parcel src/index.html
```

Alternatively, we can specify it in the `source` field in the `package.json`.

```json
{
	"source": "src/index.html"
}
```

---
#### Internal Links
[[2022-08-10]], [[JavaScript]], [[TypeScript]], [[Build Tools]]