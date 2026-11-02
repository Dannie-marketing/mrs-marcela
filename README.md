# Mrs. Marcela · Website

Static website for Marcela Laliberte, M.A. ("Mrs. Marcela"), Multilingual School Adjustment Counselor in Massachusetts.
Plain HTML, CSS and JavaScript. No build step, no dependencies.

## Structure

```
index.html              All pages: Home, About, Kids' Corner (switched with #links)
assets/css/styles.css   Styles, including the embedded font declarations
assets/js/main.js       Navigation, language switch, timeline, tabs, door, weather check-in, breathing, filters, sign-up form
assets/fonts/           Fraunces (headings) and Figtree (text), self-hosted
assets/img/             Photos, Skiby illustration, favicon
.nojekyll               Tells GitHub Pages to serve files as they are
```

## Publish on GitHub Pages

1. Create a new repository on GitHub (for example `mrs-marcela`).
2. Upload the contents of this folder to the root of the repository (drag and drop on github.com, or `git push`).
3. In the repository go to **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, branch `main`, folder `/ (root)`, and save.
5. After a minute the site is live at `https://<your-user>.github.io/<repository>/`.

### Custom domain (optional)

In **Settings → Pages → Custom domain**, enter the domain (for example `mrsmarcela.com`) and follow GitHub's DNS instructions. Then turn on **Enforce HTTPS**.

## Before launch

- **Email capture.** Open `assets/js/main.js` and fill in:
  - `FORM_ENDPOINT`: the endpoint of a form service, for example a free Formspree form (`https://formspree.io/f/xxxxxx`). Sign-ups are then sent there.
  - `CONTACT_EMAIL`: the real contact address. While `FORM_ENDPOINT` is empty, the form opens the visitor's email app addressed to this email.
- **Contact email in the page.** Replace `hello@mrsmarcela.com` in `index.html` (footer and contact links).
- **Sharing preview.** In `index.html`, change `og:image` to the full address of the image once the site is live (for example `https://mrsmarcela.com/assets/img/p_hero.webp`).
- **Sample content to confirm:** service offerings, Kids' Corner titles ("Skiby and the Storm Inside", "Feelings Weather Chart", "Calm-Down Breathing Cards", "My World of Possibilities", "Friendship Fix-It Wheel", "Family conversation starters").

## Editing tips

- Texts live in `index.html`. The hero translations (English, Spanish, Portuguese), the timeline stories and the "How I can help" tabs live in `assets/js/main.js` (look for `HL`, `TL` and `AUD`).
- Colors and type sizes are defined at the top of `assets/css/styles.css` (`--green`, `--coral`, `--sun`, `--fs-display`, etc.).
