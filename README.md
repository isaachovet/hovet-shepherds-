# Hovet Shepherds landing page

A forward-facing landing page for Isaac and Donia Hovet's donor-supported work as Standing Stone Shepherds. The page serves two primary audiences: ministry leaders and spouses seeking confidential care, and people who want to make that care possible through financial partnership.

The 2026 redesign follows the Standing Stone brand system, foregrounds testimonies, and gives visitors three clear actions:

- receive care;
- partner financially;
- join the Hovets' email list.

## Project Structure

- `index.html` contains the full one-page site, copy, navigation, calls to action, and Netlify contact form
- `thank-you.html` confirms successful form submissions
- `styles.css` contains the Standing Stone visual system, responsive layout, and accessibility styling
- `script.js` adds mobile navigation, restrained scroll reveal behavior, and the current footer year
- `netlify.toml` tells Netlify to publish this folder directly

## Primary links

- Care contact: the Netlify form on the landing page
- Financial partnership: `https://standingstone.givevirtuous.org/donate/shepherd-donation?projectCodePreselect=2102.82`
- Email list: `https://mailchi.mp/2d053c3e97a3/hovet-ministries-landing-page`
- Pastoral reflections: `https://hovetshepherds.substack.com`

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
