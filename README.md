# title

This is a starter template for [Learn Next.js](https://nextjs.org/learn).

## memo

### `getStaticProps`

- getStaticProps` only runs on the server-side.
  - It will never run on the client-side.
  - It won’t even be included in the JS bundle for the browser.
  - That means you can write code such as direct database queries   without them being sent to browsers.
- Development vs. Production
  - In development (npm run dev or yarn dev), getStaticProps runs on every request.
  - In production, getStaticProps runs at build time. However, this behavior can be enhanced using the fallback key returned by getStaticPaths
  - Because it’s meant to be run at build time, you won’t be able to use data that’s only available during request time, such as query parameters or HTTP headers.
- `getServerSideProps`
  - To use Server-side Rendering, you need to export getServerSideProps instead of getStaticProps from your page.
- Client-side Rendering
  - If you do not need to pre-render the data, you can also use the following strategy
    - dashboard pages
    - SEO is not relevant. doesn't need to be pre-rendered.
- SWR
  - We highly recommend it if you’re fetching data on the client side. It handles caching, revalidation, focus tracking, refetching on interval, and more.

## other
