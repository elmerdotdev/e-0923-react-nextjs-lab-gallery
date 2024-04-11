# E-0923 React NextJS Lab - Gallery

Goal: Create a gallery page using NextJS similar to Unsplash. Recreate the site shown on the demo video as much as you can

Demo: [https://drive.google.com/file/d/1QQgcX9hPnKsV48KKYS8AE7x5cHQG_QPR/view?usp=sharing]

## Instructions

1. Create a `dev` branch after accepting the assignment
2. Clone the repository to your local and switch to the `dev` branch
3. Create a NextJS project by running `npx create-next-app@latest`. Name your app **nextjs-gallery**
4. Create a route/folder called `/gallery` inside your *app* directory
5. Create a navigation component so that it is easier to switch between your home and gallery pages. Use `<Link></Link>` component from 'next/link' instead of `<a></a>`
6. Fetch the photos from `https://jsonplaceholder.typicode.com/photos` and display the thumbnails in the gallery page
7. Each image should be clickable. Create a dynamic route for the photo detail page
8. Clicking on an image will open a modal created using a Parallel+Intercepting route
9. Refreshing the page while the modal is open should load the actual photo detail page
10. Push your changes once you are done, create a PR, and merge `dev` to `master`

## Important Notes

- Use TailwindCSS classes to style your elements
- Every time you make changes to your parallel and intercepting route, make sure to run `npm run dev` again
- Use the `<Image />` component from 'next/image' to display an image. Do **NOT** use `<img>`. Here is the link to their documentation [https://nextjs.org/docs/pages/api-reference/components/image]
- Make sure to replace the code inside your `next.config.mjs` file with the code below. You need to do this so that you can use `<Image />` with the images provided by `jsonplaceholder.typicode.com`:

```js
/** @type {import('next').NextConfig} */
const nextConfig = {
  images: {
    domains: ['via.placeholder.com'],
  },
};

export default nextConfig;
```

## Resources

- For all photos: [https://jsonplaceholder.typicode.com/photos]
- For individual photos by id: [https://jsonplaceholder.typicode.com/photos/1]
- Code-along: [https://github.com/elmerdotdev/nextjs-day-2-code-along]
