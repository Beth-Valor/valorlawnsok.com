# Valor Lawn & Landscape — clean, professional website

A responsive, single-page website for `valorlawnsok.com`. It uses a clean green-and-gold style, mobile navigation, phone/email links, eight service categories, a sample photo gallery, and a quote-request form.

## Files
- `index.html` — all website content and quote form
- `styles.css` — layout, colors, and mobile styling
- `script.js` — mobile menu and automatic footer year
- `CNAME` — custom domain for GitHub Pages
- `assets/` — original SVG mark and favicon

## Important before launch
1. **Test the quote form.** It uses FormSubmit (a third-party service) to email `jimmy@valorlawnsok.com`. After the first real submission, check the inbox and spam folder for a FormSubmit activation email and approve it if requested. Then submit another test from a different browser/device and confirm the email arrives. Do not advertise the form until this works.
2. **Replace stock photos.** The current gallery and background images are illustrative stock photos, not confirmed Valor projects. Replace them with your own photos when available. The photos are loaded from external image URLs, so they need internet access.
3. **Review details.** Confirm all services and your service area. No fake testimonials, reviews, prices, or guarantees are included.
4. **Protect email delivery.** Do not delete or replace existing MX records or email-related TXT records when connecting the domain.
5. This is a static lead-generation site. It does not process payments or schedule jobs.

## Free publishing using GitHub Pages

### 1. Create a repository
- Go to https://github.com and sign in or create a free account.
- Create a new **public** repository named `valorlawnsok.com`.

### 2. Upload the files
- Unzip this package on your computer.
- In your repository, choose **Add file → Upload files**.
- Upload the *contents* of this folder. `index.html` must be directly in the repository root beside `styles.css`, `script.js`, and `CNAME`; include the `assets` folder.
- Commit the upload.

### 3. Enable GitHub Pages
- Open repository **Settings → Pages**.
- Under Build and deployment, choose **Deploy from a branch**.
- Select branch `main` and folder `/(root)`, then save.
- Wait for the temporary `github.io` site to deploy.

### 4. Set the custom domain
- In **Settings → Pages → Custom domain**, enter `valorlawnsok.com` and save.
- Do this before changing DNS at Namecheap. Keep the included `CNAME` file in the repository root.

### 5. Configure DNS at Namecheap
- Sign in at https://www.namecheap.com.
- Open **Domain List → Manage** beside `valorlawnsok.com`, then **Advanced DNS**.
- If your nameservers point somewhere other than Namecheap DNS, make DNS changes at the current DNS provider instead.
- Add four `A Record` entries:
  - Host `@` → `185.199.108.153`
  - Host `@` → `185.199.109.153`
  - Host `@` → `185.199.110.153`
  - Host `@` → `185.199.111.153`
- Add one `CNAME Record`:
  - Host `www`
  - Value `YOUR-GITHUB-USERNAME.github.io` (replace with your actual GitHub username; do not add a repository name).
- Remove only conflicting web records for `@` or `www` after checking what they do. **Do not delete MX records or email-related TXT records.**
- Save changes. DNS can take up to 24 hours to propagate.

### 6. Enable HTTPS
- Return to **Settings → Pages**.
- Wait for GitHub's DNS check and certificate setup to complete.
- Check **Enforce HTTPS**.
- Test `https://valorlawnsok.com` and `https://www.valorlawnsok.com`.

Official help:
- GitHub Pages custom domains: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site
- Namecheap GitHub Pages setup: https://www.namecheap.com/support/knowledgebase/article.aspx/9645/2208/how-do-i-link-my-domain-to-github-pages/

## Before you share the website
- [ ] `https://valorlawnsok.com` loads
- [ ] `www` address loads or redirects as expected
- [ ] HTTPS is active
- [ ] Call buttons work on mobile
- [ ] Email links open a mail app
- [ ] Quote form email is activated and tested
- [ ] Replace stock images with your own project photos when ready
- [ ] Test mobile menu and form layout
- [ ] Confirm service area and business details

## How to edit later
- Change page wording in `index.html`.
- Change colors and layout in `styles.css`. Main colors are at the top in `:root`.
- To use your own photos, upload them into `assets/` and change the image URLs in `index.html` and the CSS hero/about backgrounds.
- Upload changed files to the same repository and commit. GitHub Pages automatically republishes.
