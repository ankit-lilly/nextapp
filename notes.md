## How Routing and Navigation Works

The App Router uses a hybrid approach for routing and navigation. On the server, your application code is automatically code-split by route segments. 
And on the client, Next.js prefetches and caches the route segments.


This means that when the user navigates to a  new route, the browser doesn't reload the page, and only the route segments that change re-render - improving hte navigation experience and performance.



1. Code Splitting:


Code splitting allows you to split your application code into smaller bundles
to be downloaded and executed by the browser. This reduces the amount of dataa
transferred and execution time for each request, leading to improved 
performance.

Server components allow for your application code to be automatically code-split by route segments. This means only the code needed for the current route
is loaded on navigation.


2. Prefetching

Prefetching is a way to preload a route in the background before the user visits it.

There are two ways routes are prefetched in the Next.js.

- <Link> component: Routes are automatically prefetched as they become visible in user's viewport. Prefetching happens when the page first loads or when it comes into view through scrolling.

- router.prefetch(): The useRouter hook can be used to prefetch routes programmatically.


