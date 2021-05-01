# dadjokes


## Project Creation

```bash
# creating nuxt app (universal)
$ npx create-nuxt-app dadjokes

# get into project and run it
$ cd app dadjokes & npm run dev

# there are LAYOUT and PAGES folder. 
# Pages are using layout, and we create ie. About folder in pages, and index.vue in About folder. This way, vue router is automatically set itself.
$ using <nuxt-link to='/about'> About </nuxt> 

#using head() for title, meta tags
$ export default {
 head() {...}
}

```

## Build Setup

```bash
# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm run start

# generate static project
$ npm run generate
```

For detailed explanation on how things work, check out [Nuxt.js docs](https://nuxtjs.org).
