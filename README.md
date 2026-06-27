# The Goodness of Hemp Partner Email

This folder is ready to publish with GitHub Pages as a small static partner-email kit.

## Files

- `index.html` is the GitHub Pages preview entrypoint.
- `goh_partner_email.html` is the reusable email HTML template.
- `header-logo.png`, `video-thumbnail.jpg`, `capitol-icon.png`, `goh-card-logo.png`, and the `social-*.png` files are the hosted email assets.
- `.nojekyll` tells GitHub Pages to publish the files exactly as-is.

## Publish On GitHub Pages

1. Create a new GitHub repository, or use an existing public repository.
2. Add every file from this folder to the repository root.
3. Commit and push to the `main` branch.
4. In GitHub, open the repo, then go to `Settings` > `Pages`.
5. Under `Build and deployment`, choose `Deploy from a branch`.
6. Select branch `main` and folder `/root`, then save.
7. Your preview URL will usually be:

```text
https://YOUR_USERNAME.github.io/YOUR_REPO/
```

GitHub says Pages sites publish static files from a repository, use `index.html` as an entry file, and may take a few minutes to update after a push:
https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site

## Use In Mailchimp Or Another Email Platform

The hosted preview can use local filenames like:

```html
<img src="header-logo.png" alt="WYNK x The Goodness of Hemp">
```

But pasted email HTML should use absolute public image URLs, like:

```html
<img src="https://YOUR_USERNAME.github.io/YOUR_REPO/header-logo.png" alt="WYNK x The Goodness of Hemp">
```

After the GitHub Pages site is live, replace each image `src` in the email template with its full URL:

```text
https://YOUR_USERNAME.github.io/YOUR_REPO/header-logo.png
https://YOUR_USERNAME.github.io/YOUR_REPO/video-thumbnail.jpg
https://YOUR_USERNAME.github.io/YOUR_REPO/capitol-icon.png
https://YOUR_USERNAME.github.io/YOUR_REPO/goh-card-logo.png
https://YOUR_USERNAME.github.io/YOUR_REPO/social-x.png
https://YOUR_USERNAME.github.io/YOUR_REPO/social-facebook.png
https://YOUR_USERNAME.github.io/YOUR_REPO/social-instagram.png
https://YOUR_USERNAME.github.io/YOUR_REPO/social-linkedin.png
https://YOUR_USERNAME.github.io/YOUR_REPO/social-tiktok.png
https://YOUR_USERNAME.github.io/YOUR_REPO/social-truth.png
https://YOUR_USERNAME.github.io/YOUR_REPO/social-website.png
```

Do not use `raw.githubusercontent.com` URLs for production email campaigns. GitHub Pages URLs are cleaner and serve the expected web asset types.

## Video Module

The email uses a static video thumbnail image with a play-button overlay. The whole thumbnail links to YouTube:

```text
https://www.youtube.com/watch?v=W27A8U_x5ig
```

This is the most reliable approach for Mailchimp and major email clients because many inboxes strip or ignore embedded video.

## Hosting Recommendation

GitHub Pages is good for a partner kit, previews, and light asset hosting. For a large email blast, Mailchimp Content Studio or a CDN is safer because inbox image traffic can be heavy. GitHub documents Pages usage limits, including a 1 GB published-site limit and a 100 GB/month soft bandwidth limit:
https://docs.github.com/en/pages/getting-started-with-github-pages/github-pages-limits
