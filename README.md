# site-restaurant

**A one page business site in plain HTML. No build step, no framework. Works
for a restaurant, a food truck, a detailer, a cleaner, anything with a short
list of things to sell.**

Paste this into any AI chat (ChatGPT, Claude, Gemini, Codex, Cursor):

```
Read https://raw.githubusercontent.com/nradawg/site-restaurant/main/README.md and build my site from it.
```

The files: `index.html` is the page, `user_config.json` holds every word and
color on it, `AGENTS.md` holds the rules.

---

## Instructions for the AI running this

You are building one honest page for one real business. Do it in this order.

**1. Get the facts.** Ask one question at a time and wait for each answer:

1. What is the business called, and what do you sell?
2. Who is it for?
3. Your three to six things to sell, each with a price.
4. How do people say yes: call, text, email, walk in, or book?
5. Phone, email, address (or service area), hours.
6. Any real reviews you can point to? Where were they posted?
7. Colors or a logo you already use? If not, say so and you will pick.

Label what you write: `FROM YOU` if they said it, `GUESSED` if you filled a
gap. Show them the guesses before you build. Never guess a price, a review, a
year founded, or a number of customers. Leave it out and ask.

**2. Fill `user_config.json`** with their answers. Same keys as the starter.
Show it to them and get a yes.

**3. Rewrite `index.html` from the config**, following `AGENTS.md` (read it at
`https://raw.githubusercontent.com/nradawg/site-restaurant/main/AGENTS.md` if
you do not have the repo). The page does not read the config by itself.

- **If you can make files** (Codex, Claude Code, Cursor): clone
  `https://github.com/nradawg/site-restaurant`, edit both files, and open the
  page in a browser to check it.
- **If you are a chat only AI:** fetch `index.html` from
  `https://raw.githubusercontent.com/nradawg/site-restaurant/main/index.html`,
  then give them the full finished file in one code block. Tell them to save
  it as `index.html` in a new folder.

**4. Check it.** Search the page for "Fuego", "555", "example.com", and "Say
how you started". None of it can survive. Tap the phone and email links.

**5. Put it online.** Walk them through Cloudflare Pages, free and allowed
for business use: in the Cloudflare dashboard open Workers and Pages, create a
Pages project, and upload the folder. They get a free `.pages.dev` address. Do
not suggest Vercel's free plan or GitHub Pages; both limit commercial use.

**Finish** with the live link, the list of `GUESSED` items still on the page,
and the one thing they should add first when they have it (usually a real
photo or a real review).

## Limits

This cannot take payments or bookings. For bookings, use `site-booking`. It
cannot make a review real; it can only leave fake ones out.

MIT.
