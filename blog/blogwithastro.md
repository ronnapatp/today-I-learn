# Create my blog page with [astro](https://astro.build/)

I learned about astro that astro have framwork for blog

## Docs
[Click here](https://docs.astro.build/getting-started)

## To build astro
With npm
``` shell
$ npm init astro
$ npm install astro # Install node module
$ npm start # to start dev sever
$ npm run build # build astro ./dist
```
With yarn
``` shell
$ yarn create astro
$ yarn # Install node module
$ yarn start # to start dev sever
$ yarn run build # build astro ./dist
```
[Click here to read more](https://docs.astro.build/installation)

# Blog
Start with :
``` javascript
let title = 'Ronnapatp blog';
let description = 'Story of my life in blog page';
let permalink = 'https://example.com/';

```
Add public date :
``` javascript
// Data Fetching: List all Markdown posts in the repo.
let allPosts = Astro.fetchContent('./posts/*.md');
allPosts = allPosts.sort((a, b) => new Date(b.publishDate) - new Date(a.publishDate));
```
### Add post with `markdown` file
``` markdown
---
title: 'Building this astro website page'
description: "We're excited to announce Astro as a new way to build static websites and deliver lightning-fast performance without sacrificing a modern developer experience."
publishDate: 'Sunday, August 14 2021'
author: 'ronnapatp'
heroImage: '/social.jpg'
alt: 'Astro'
layout: '../../layouts/BlogPost.astro'
---

My first blog in my frist blog website — _chill_.

This is first blog website for me using [astro framwork](https://astro.build/) to build and host at [vercel.com](https://vercel.com/) or [firebase from google](https://console.firebase.google.com/)

About to contribute this project please go to [github]() 
```

### Package.json file
``` json
{
  "name": "@example/blog",
  "version": "0.0.1",
  "private": true,
  "scripts": {
    "start": "astro dev",
    "build": "astro build"
  },
  "devDependencies": {
    "astro": "^0.18.13",
    "@astrojs/renderer-preact": "^0.2.1"
  }
}
```


[Read more about astro >>>](https://astro.build/blog/introducing-astro)
