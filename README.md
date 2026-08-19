# The Sol Ring Scoop — parody site

**This is a joke site.** "The Sol Ring Scoop" is a fictional publication. The article
about Primeval Titan being unbanned in Commander is fabricated, as is every byline,
quote, comment, and advertisement on it. No leak occurred and no such announcement
exists. Built as a personal prank between friends.

Magic: The Gathering is a trademark of Wizards of the Coast LLC. This site is
unofficial fan content, not produced by or affiliated with Wizards of the Coast.

`robots.txt` disallows all crawlers and both pages carry `noindex`, so it should not
turn up in search results.

## Structure

```
index.html                                     homepage
commander/primeval-titan-unban-leak/index.html the article
og-image.png                                   1200x630 link preview card
robots.txt                                     blocks crawlers
.nojekyll                                      tells GitHub Pages to serve files as-is
```

## Before deploying

Both HTML files contain a line marked `EDIT ME`. Replace every instance of
`https://solringscoop.com` with the URL you actually host at. The `og:image` tag in
particular must be an absolute URL or the link preview card will not render in
iMessage, Discord, or Slack.

## Deploying

**GitHub Pages** — from this folder, with the GitHub CLI already authenticated:

```bash
git init -b main
git add .
git commit -m "Initial commit"
gh repo create solringscoop --public --source=. --push
```

Then in the repo: Settings → Pages → Source: "Deploy from a branch" → `main` / `/ (root)`.
Live in a minute or two at `https://<username>.github.io/solringscoop/`.

Note that a project-path URL is a giveaway. A repo named `<username>.github.io`
serves from the domain root instead, and a custom domain is better still.

**Netlify** — drag this folder onto netlify.com/drop. No account needed to start,
and a custom domain can be attached afterward.
