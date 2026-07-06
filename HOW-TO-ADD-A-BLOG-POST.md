# How to Add a New Blog Post Each Month

Your site now has a blog with 3 starter articles. To keep improving your SEO,
aim to publish **1 new article per month**. Here's the exact process.

The easiest way: just tell Claude what topic you want to write about, and
paste this guide in — Claude can generate the whole post for you. But if you
want to do it yourself (or edit one Claude wrote), here's how it works.

---

## The 5 steps

### 1. Duplicate the template
Copy `blog/post-template.html` and rename it to your new post's slug, e.g.:

```
blog/why-travel-insurance-matters-for-family-trips.html
```

Use lowercase words separated by hyphens — no spaces, no special characters.
This filename becomes part of the URL, so make it describe the topic clearly.

### 2. Fill in the details at the top of the file
Open the new file and update these parts:
- `<title>` tag
- `<meta name="description">` — a 1–2 sentence summary (shows up in Google search results)
- `<link rel="canonical">` — update the filename to match
- The JSON-LD schema block (`headline`, `description`, `datePublished`, `mainEntityOfPage`)
- The breadcrumb tag name (e.g. "Travel Insurance")
- The `<h1>` title
- The article-meta line (date and estimated read time)

### 3. Write the body content
Replace the placeholder paragraphs inside `<div class="article-body-wrap article-body">`
with your real content. Keep using the same tags:
- `<h2>` for section headings
- `<p>` for paragraphs
- `<ul><li>` for bullet lists
- `<blockquote>` for a key takeaway or tip

Aim for 500–900 words. Real, useful, specific advice (not generic filler)
is what actually helps SEO and builds trust with readers.

### 4. Update the "Related Articles" links at the bottom
Swap in 2 of your other posts so readers can click through to more content.

### 5. Add the new post to 3 places
1. **`blog.html`** — copy one of the `<a class="blog-card">` blocks and update
   the title, tag, date, excerpt, and link.
2. **`index.html`** — optionally swap one of the 3 homepage teaser cards
   (inside `<section id="insights">`) for your newest post, so the homepage
   always shows fresh content.
3. **`sitemap.xml`** — copy one of the `<url>` blocks, update the `<loc>` to
   your new post's URL and `<lastmod>` to today's date. This helps Google
   discover and index the new post faster.

---

## Topic ideas to keep the monthly habit going
- Seasonal: "Flood season checklist for Sabah homeowners" (before monsoon)
- Seasonal: "Planning a year-end trip? Here's what travel insurance actually covers"
- FAQ-style: "What happens if I miss a premium payment?"
- Myth-busting: "5 motor insurance myths that could cost you at claim time"
- Local: "Do I need insurance for a rented apartment in Kota Kinabalu?"
- Comparison: "Named perils vs all risks — what's the difference?"

A simple, honest, locally-relevant article beats a long generic one every time.

---

## Quick reminder for Claude
If you're using Claude to help write the next post, you can just say:
> "Add a new blog post about [topic]. Follow the same structure as the
> existing posts in /blog/, and update blog.html, the homepage, and
> sitemap.xml too."
