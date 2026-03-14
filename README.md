# HEPEG Website

**Health Economics and Policy Evaluation Group**

A clean, multi-page static website. No build tools, no dependencies — just HTML and CSS.

---

## Files

```
hepeg-site/
├── index.html          ← Homepage
├── events.html         ← Events page
├── projects.html       ← Research projects
├── publications.html   ← Publications list
├── team.html           ← Team members
├── contact.html        ← Contact form + mailing list
├── style.css           ← Shared stylesheet
└── README.md           ← This file
```

## How to Deploy on GitHub Pages (Free)

1. **Create a GitHub account** at https://github.com if you don't have one
2. **Create a new repository** named `hepeg-site` (or `hepeg.github.io` for a cleaner URL)
3. **Upload all files** (drag and drop them into the repository)
4. Go to **Settings → Pages**
5. Under "Source", select **main branch** and click Save
6. Your site will be live at `https://YOUR-USERNAME.github.io/hepeg-site/`

### Custom Domain (optional, recommended)

1. Buy a domain like `hepeg.org` from any registrar (~€10/year via Namecheap, Porkbun, etc.)
2. In your domain registrar, add a CNAME record pointing to `YOUR-USERNAME.github.io`
3. In GitHub repo Settings → Pages, enter your custom domain
4. GitHub will auto-provision HTTPS

## How to Update Content

Every page has HTML comments (`<!-- ... -->`) explaining exactly what to copy-paste to add new items. The general pattern:

### Add a new event:
1. Open `events.html`
2. Find the comment `HOW TO ADD A NEW EVENT`
3. Copy one `<div class="event-item">` block
4. Paste it, update the date/title/description

### Add a new publication:
1. Open `publications.html`
2. Copy one `<li class="pub-item">` block
3. Paste at the top of the list, update details

### Add a new team member:
1. Open `team.html`
2. Copy one `<div class="team-card">` block
3. Paste it, update name/role/bio
4. For photos: save image in an `images/` folder, update the `<img>` tag

### Add a new project:
1. Open `projects.html`
2. Copy one `<div class="card">` block inside the card-grid
3. Update title, coordinator, description, link

## Setting Up Mailchimp (Mailing List)

1. Create a free account at https://mailchimp.com (free up to 500 contacts)
2. Go to **Audience → Signup forms → Embedded forms**
3. Customize the form, then copy the HTML code
4. Replace the placeholder `<form>` blocks in:
   - `index.html` (newsletter CTA section)
   - `events.html` (bottom CTA)
   - `contact.html` (mailing list section)

## Setting Up Contact Form

The contact form in `contact.html` uses [Formspree](https://formspree.io):

1. Sign up at https://formspree.io (free tier: 50 submissions/month)
2. Create a new form and get your form ID
3. In `contact.html`, replace `YOUR_FORM_ID` in the form action URL

## Adding Team Photos

1. Create an `images/` folder in the project
2. Save photos as `firstname-lastname.jpg` (keep them under 200KB each)
3. In `team.html`, replace the placeholder `<div class="avatar">` with:
   ```html
   <img class="avatar" src="images/firstname-lastname.jpg" alt="Name">
   ```

## Fonts

The site uses Google Fonts (loaded from CDN, no files to host):
- **DM Serif Display** — headings
- **IBM Plex Sans** — body text
