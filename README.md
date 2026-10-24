# Parcel — Next.js product showcase

Take-home assignment: a small store built with the Next.js App Router, using
the [FakeStore API](https://fakestoreapi.com/docs).

## Requirements checklist

| Requirement | Where |
| --- | --- |
| Home page `/` with 5 products (image, name, "View Details") | `src/app/page.jsx`, `src/components/ProductCard.jsx` |
| Product detail page `/products/[slug]` | `src/app/products/[slug]/page.jsx` |
| Navigation with `<Link>` (Home, Contact) | `src/components/Header.jsx`, `src/app/contact/page.jsx` |
| "Add to Favorite" with `useState` + `useEffect` | `src/lib/useFavorites.js`, `src/components/FavoriteButton.jsx` |
| Optional: search | `src/components/ProductBrowser.jsx` (searches all 20 products) |
| Optional: styling | `src/app/globals.css` |

## How it works

- Slugs look like `mens-casual-slim-fit-2`. The trailing number is the product
  id used to call `GET /products/:id`.
- Favorites are saved in `localStorage`, so they survive a refresh. The header
  count updates live.
- Product data is cached for one hour (`revalidate`).

## Run locally

```bash
npm install
npm run dev
```
<!-- 
Open http://localhost:3000. -->

<!-- ## Deploy

1. Create a GitHub repo and push this folder:
   ```bash
   git init && git add . && git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/<you>/parcel-store.git
   git push -u origin main
   ```
2. Go to https://vercel.com/new, import the repo, and click Deploy
   (no environment variables needed).

## Font

Proxima Nova Regular is loaded locally from `src/fonts/proximanova_regular.ttf`
with `next/font/local` (see `src/app/layout.jsx`). Check the license in
`src/fonts/COPYRIGHT.txt` before publishing the repo publicly. -->
