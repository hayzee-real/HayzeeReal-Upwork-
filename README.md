# Ibrahim Azeez Adebowale, Book Editing Site

Single file site. Everything lives inside `index.html`: the CSS, the JavaScript, and the
portrait photo (embedded as a data URI). There are no image files and no build step.

Live at **https://hayzee-real-upwork.vercel.app/**

Files in this repo, all at the root, never inside a folder:

```
index.html     the whole site
robots.txt     tells search engines and AI answer engines they may read the site
sitemap.xml    tells Google the one page that exists and when it last changed
README.md      this file, for you only, it is not part of the site
```

---

## Updating the site

Vercel is connected to this GitHub repo, so GitHub is the only place you touch.

1. Open the repo on GitHub.
2. Click **Add file**, then **Upload files**.
3. Drag in the new `index.html`. GitHub replaces the old one because the name matches.
4. Scroll down, write a short commit message, click **Commit changes**.

Vercel redeploys automatically in about thirty seconds. You never open the Vercel
dashboard again.

If the site looks unchanged after a minute, hard refresh the page. On a phone that is
usually a pull down refresh, on a laptop it is Ctrl+Shift+R or Cmd+Shift+R.

---

## The colours

They are set once at the top of `index.html`, inside `:root`. Change a value there and it
changes everywhere on the site.

| Name | Code | Where it shows |
|---|---|---|
| Deep navy | `#172434` | nav bar, hero, Real Edits band, contact section |
| Champagne gold | `#C4A674` | buttons, badges, the italic hero line, small accents |
| Warm stone | `#E4E1DC` | the alternating page background |
| White | `#FFFFFF` | the cards sitting on stone |

Gold buttons carry navy text on purpose. Gold on white is hard to read.

---

## Things you may want to change

| What | Search `index.html` for |
|---|---|
| Hourly rate | `$35` |
| Pricing cards | `id="pricing"` |
| Stats in the hero | `class="stat"` |
| Client quotes | `class="quote"` |
| The eleven real edits | `class="rec"` |
| FAQ answers | `class="qa"` |
| Turnaround estimator speeds | `var RATE` |
| WhatsApp number | `2349167856753` (four places) |
| Email address | `hayzeerealfemi@gmail.com` |
| Upwork profile link | `upwork.com/freelancers` |

**Important:** the FAQ appears twice, once as visible text and once inside the structured
data block near the bottom of the file. If you change an answer in one place you must
change it in the other, or Google and the AI answer engines see a mismatch and trust the
page less.

---

## After any big change

1. Open the site on a phone, not just a laptop. Tap the WhatsApp link, the email link and
   both buttons on the form.
2. If you changed the wording of a service or the FAQ, resubmit the sitemap in **Google
   Search Console** so the new text is picked up sooner.

---

## Google Search Console, one time setup

1. Go to search.google.com/search-console and click **Add property**.
2. Choose **URL prefix** and paste `https://hayzee-real-upwork.vercel.app/`.
3. Verify with the **HTML tag** method. Google gives you a `<meta>` line. Paste it into
   `index.html` just under the `<head>` line, commit, wait a minute, then click Verify.
4. Once verified, open **Sitemaps** in the left menu and submit `sitemap.xml`.

This is what gets the site showing up when someone searches your name, which matters
because clients do search your name after reading your Upwork profile.

---

## Adding a custom domain later

Buy the domain, then in Vercel go to **Project, Settings, Domains**, add it, and follow
the DNS records Vercel shows you. Vercel issues the HTTPS certificate itself.

Then update the address in four places and commit: the `canonical` tag in `index.html`,
`og:url` in `index.html`, the `Sitemap:` line in `robots.txt`, and the `<loc>` line in
`sitemap.xml`. Add the new domain as a second property in Search Console too.
