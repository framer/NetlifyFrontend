## Framer Netlify Frontend Example

This is a little example project that allows you to combine multiple Framer sites under a single domain like:

```
mysite.com/demo1 → demo1.framer.app
mysite.com/demo2 → demo2.framer.app
mysite.com/demo3 → demo3.framer.app
```

The technology required for this is called rewriting and is offered by a variety of hosting companies like Netlify, Vercel, CloudFront or CloudFlare. This example uses Netlify because it's free an easy.

## Setup

[Netlify offers rewrites](https://docs.netlify.com/routing/redirects/rewrites-proxies/) and requires to configure them in your [`_redirects`](https://github.com/framer/NetlifyFrontend/blob/main/static/_redirects) file.

In the file we configure three different Framer sites:

```
/demo1/*  https://safe-presentations-451616.framer.app/:splat  200
/demo2/*  https://exact-road-711014.framer.app/:splat  200
/demo3/*  https://spot-strive-526314.framer.app/:splat  200
```

- https://safe-presentations-451616.framer.app
- https://exact-road-711014.framer.app
- https://spot-strive-526314.framer.app

You can try these out in the live deploy:

- https://snazzy-arithmetic-9c136d.netlify.app/demo1
- https://snazzy-arithmetic-9c136d.netlify.app/demo2
- https://snazzy-arithmetic-9c136d.netlify.app/demo3
