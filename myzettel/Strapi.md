---
template: note
last_reviewed: "2022-12-31"
---
![tp.web.random_picture](https://images.unsplash.com/photo-1590328890650-1c94261ff33e?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYzODUwNTM3&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-09-22) | (time:: 18:12) | (weather:: Vadodara: ☀️   +34°C ↗17km/h)

# Strapi
Strapi is a headless CMS based on Node.js. It has out-of-the-box support for REST and GraphQL API.

## New project
```shell
npx create-strapi-app <app-name>
```

This will create a new Strapi project. It will be launched automatically in your browser.

## Run in `development` mode
Run the `develop` npm task that Strapi creates by default when you create a new project.

```shell
npm run develop
```

## Content Type Builder
Use the *Content-Type Builder* plugin to set up your content-type blueprint. For example, a `Blog` content type would have `title`, `body`, and `author` fields. All of those fields would be `text` fields.

### Collection Type
These are types that will have more than one occurrence on your site. For example, we have more than one blog post on our blog.

### Single Type
This type is for a unique piece of content. For example, the *Home page* or *About page*.

### Component 
A component is a field that you might use in many different collection types. Under this section, we create components for use inside multiple *Collection Types*.

---
## Internal Links
[[2022-09-22]], [[Node.js]], [[CMS]] 