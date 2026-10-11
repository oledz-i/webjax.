# WebJax Inc. — Website

A single-page, static website for **WebJax Inc.** web design services.
Everything (HTML, CSS, JavaScript, images) lives in one file: `index.html`.
The Portfolio is a second "page" inside that same file. It opens when someone clicks a Portfolio button, and the browser's back button works.

## Deploy on Netlify (takes about 2 minutes)

1. Go to <https://app.netlify.com> and sign in (free account is fine).
2. Click **Add new site → Import an existing project** and pick this GitHub repo.
   - Or drag-and-drop the folder containing `index.html` onto the Netlify dashboard.
3. Leave the build settings blank (there is no build step). Publish directory: `.`
4. Click **Deploy**. You get a live `something.netlify.app` URL right away.
5. Optional: **Domain settings → Add custom domain** to connect `webjax.com` or similar.

## Get contact-form messages in your inbox

The contact form uses **Netlify Forms** (already wired up in `index.html`).

1. After the first deploy, open your site in Netlify and go to **Forms**.
   You should see a form named `contact`.
2. Go to **Site configuration → Forms → Form notifications → Add notification → Email notification**.
3. Enter `webjaxmedia@gmail.com` and save.

From then on, every submission is emailed to you and also stored in the Netlify dashboard.
Netlify's free plan includes 100 submissions per month.

If the site is ever hosted somewhere other than Netlify, the form automatically
falls back to opening the visitor's email app with the message pre-filled and
addressed to `webjaxmedia@gmail.com`.

## Editing the site

Open `index.html` in any text editor. Things you'll most likely want to change:

| What | Where to look |
| --- | --- |
| Prices and package features | the `<section id="pricing">` block |
| Contact email | search for `webjaxmedia@gmail.com` |
| Portfolio page | the `<main id="portfolio">` block (the page that opens from the Portfolio buttons). Copy the project block to add another demo. |
| Portfolio preview image on the home page | the two `<img>` tags in `<section id="work">` |
| Colors | the `:root { ... }` block at the top of the `<style>` tag |
| Motto / bio text | the `<section id="about">` block |

## Preview locally

Just double-click `index.html`, or run a tiny server:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```
