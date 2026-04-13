# hovetshepherds-site

A simple, deployable static website for `hovetshepherds.com`, built for Netlify with plain HTML, CSS, and a small amount of JavaScript.

## Project Structure

- `index.html` contains the full one-page site, copy, navigation, and Netlify contact form
- `styles.css` contains the visual design, layout, responsiveness, and accessibility styling
- `script.js` adds restrained scroll reveal behavior
- `netlify.toml` tells Netlify to publish this folder directly

## Preview Locally

Open the folder and run a simple static server from inside `06 Outputs/hovetshepherds-site`:

```bash
python3 -m http.server 8000
```

Then visit:

```text
http://localhost:8000
```

You can also open `index.html` directly in a browser, but using a local server is closer to deployment behavior.

## Deploy to Netlify

1. Push this folder to a Git repository, or drag the folder into Netlify's manual deploy area.
2. In Netlify, create a new site from that repository or upload.
3. If you are deploying from the project folder itself, Netlify can publish the folder root as-is.
4. If Netlify asks for settings, use:

```text
Publish directory: .
Build command: (leave blank)
```

5. Add your custom domain `hovetshepherds.com` in Netlify domain settings.
6. Update DNS records at your domain registrar to point to Netlify.
7. If you want the contact form to send notifications, configure Netlify Forms notifications in the Netlify dashboard after the first deploy and point them to `isaac.hovet@standingstoneministry.org`.

## Updating Content Later

- Edit `index.html` first for wording, section content, contact details, and navigation labels
- Edit `styles.css` for colors, spacing, typography, and layout changes
- Update the contact email in `index.html` before launch if you want a different inbox
- Netlify form notification recipients are configured in Netlify, not in the HTML itself
- If you do not want the reveal effect, remove the `data-reveal` attributes in `index.html` or remove `script.js`
