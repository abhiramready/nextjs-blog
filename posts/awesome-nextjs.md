---
title: "Next.js is Awesome 🚀"
date: "2022-06-23"
---

### Learning [Next.js](https://nextjs.org/learn/foundations/about-nextjs)

Next.js has two forms of pre-rendering:

Static Generation and Server-side Rendering. The difference is in when it generates the HTML for a page.

- SSG Static Generation is the pre-rendering method that generates the HTML at build time. The pre-rendered HTML is then reused on each request.
- SSR Server-side Rendering is the pre-rendering method that generates the HTML on each request.

#### Client-side Rendering in Next.js

- When the page loads, fetch external data from the client using JavaScript and populate the remaining parts.
- This approach works well for user dashboard pages, for example. Because a dashboard is a private, user-specific page, SEO is not relevant, and the page doesn’t need to be pre-rendered. The data is frequently updated, which requires request-time data fetching.

#### Server-side Rendering

```
// context contains request-specific parameters.
export async function getServerSideProps(context) {
  return {
    props: {
      // props for your component
    },
  };
}
```

**Dynamic URLs:** Next.js allows you to statically generate pages with paths that depend on external data, where each page path depends on external data.

![](/images/page.png)
