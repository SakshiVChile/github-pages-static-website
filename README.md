Elevate labs task 4
# github-pages-static-website

**Task: Host a Static Website with GitHub Pages**

A simple HTML and CSS website deployed for free using GitHub Pages.

**Live website:** https://sakshivchile.github.io/github-pages-static-website/

## What I did

1. Created a new public GitHub repository.
2. Added `index.html` (the page) and `style.css` (the styling).
3. Went to **Settings -> Pages**, chose **Deploy from a branch**, selected the `main` branch and the `/ (root)` folder, and saved.
4. Waited about a minute for the "pages build and deployment" workflow to finish, then opened the live link.

## Files

- `index.html`: the page content
- `style.css`: layout, colours and fonts
- `screenshots/`: proof that the site is live

## How to update the website

Edit `index.html` or `style.css` on `main` (on GitHub or with `git push`). GitHub Pages redeploys automatically within a minute or two.

## Interview questions

**1. What is GitHub Pages?**
A free hosting service from GitHub that publishes static files (HTML, CSS, JavaScript, images) straight from a repository to a public URL.

**2. Can you host dynamic apps here?**
No. It serves only static files. There is no server-side code such as Node, PHP or Python, and no database. For dynamic apps you need a service like a VM, a container platform, or serverless functions. A static site can still call external APIs from JavaScript in the browser.

**3. What are the limits of GitHub Pages?**
Roughly: a published site should stay under about 1 GB, the monthly bandwidth is soft-limited to about 100 GB, builds are limited to about 10 per hour, and it is not meant for commercial or heavy-traffic use. Free Pages needs a public repo on a free account. (Limits can change, so check GitHub's docs.)

**4. How do you update the website?**
Commit changes to the published branch (here `main`). A GitHub Actions workflow named "pages build and deployment" redeploys the site automatically.

**5. What happens when you delete the repo?**
The site goes offline and the URL returns a 404, because the files are served from that repository. I would also lose the repo's history, so I would keep a backup.

**6. What is the default file that loads?**
`index.html` in the root of the published folder. If it is missing, the site shows a 404 page.

**7. Can you use a custom domain?**
Yes. In **Settings -> Pages** I can set a custom domain, add a `CNAME` file, and create DNS records at my domain provider. GitHub can then provide free HTTPS for it.
