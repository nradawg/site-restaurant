# Rules for the AI editing this site

`user_config.json` is the source of truth. Every word, price, photo, and color
on the page comes from it. `index.html` does not read the file by itself, so
whenever the config changes, you rewrite `index.html` to match it.

## How to apply the config

- **Name, tagline, description:** nav logo, `<title>`, meta description, Open
  Graph tags, hero, footer.
- **colors:** the three hex values in the `tailwind.config` block.
- **items:** one card per entry, in order. No image means no `<img>` in that
  card, not a stock photo.
- **about:** one paragraph per entry.
- **hours:** one line per entry.
- **phone:** the `tel:` link uses digits only with the country code, so
  `(323) 555-0187` becomes `tel:+13235550187`.
- **address:** the map is
  `https://www.google.com/maps?q=<address, URL encoded>&output=embed`. No key
  needed.
- **social:** one text link per entry that is not empty. Empty means no link.
- **reviews:** add a reviews section only when this list has entries. Each
  entry is a real review the owner can point to: first name, the words, where
  it was posted. If it is empty, there is no reviews section.

## Never

- Never write a review, testimonial, star rating, "since 20XX", award, or
  customer count that the owner did not give you. A new business with no
  reviews looks new. A new business with fake reviews looks like a scam the day
  someone checks.
- Never leave sample text from this starter on a live site. Before you call it
  done, search the page for "Fuego", "555", "example.com", and "Say how you
  started".
- Never add a framework or a build step. This stays one HTML file.

## Check before you call it done

- It reads right at 375px wide and at 1440px wide.
- One `<h1>`. Every `<img>` that shows something has alt text.
- The phone and email links work when tapped.

## Hosting

Host it on **Cloudflare Pages**, free, commercial use allowed. In the
Cloudflare dashboard open Workers and Pages, create a Pages project, and
upload this folder. Or connect the GitHub repo if they have one. They get a
free `.pages.dev` address.

Do not use Vercel's free Hobby plan or GitHub Pages for a business. Both
limit commercial use in their own terms.
