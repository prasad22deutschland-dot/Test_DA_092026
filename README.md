# Prasad Natuskar — Professional Portfolio Website

This is a responsive personal portfolio website for Prasad Natuskar, presenting his design-management experience, services, project case studies, technical skills, certifications, and contact information.

## Project files

```text
Prasad_Natuskar_Portfolio/
├── index.html
├── styles.css
├── app.js
├── README.md
└── assets/
    ├── prasad_natuskar.jpg
    ├── miraya_business_hub.jpg
    └── konar_business_park.jpg
```

The website still works if the three photographs are unavailable. Designed fallback visuals are displayed automatically instead of broken-image boxes.

## Quick start

### Option 1 — Open directly

1. Extract `Prasad_Natuskar_Portfolio.zip`.
2. Keep `index.html`, `styles.css`, and `app.js` in the same folder.
3. Double-click `index.html`.
4. The website will open in the default browser.

This is sufficient for reviewing the layout, content, tabs, animations, navigation, and responsive design.

### Option 2 — Run a local web server

A local server gives the most deployment-like result.

#### Using Visual Studio Code

1. Open the portfolio folder in Visual Studio Code.
2. Install the **Live Server** extension by Ritwick Dey.
3. Right-click `index.html`.
4. Select **Open with Live Server**.

#### Using Node.js

Open a terminal inside the portfolio folder and run:

```bash
npx serve .
```

Then open the local address shown in the terminal, normally `http://localhost:3000`.

#### Using Python

For Python 3:

```bash
python -m http.server 8000
```

On some systems the command is:

```bash
python3 -m http.server 8000
```

Then open [http://localhost:8000](http://localhost:8000).

## Add the real images

Create an `assets` folder beside `index.html` and add the following files using these exact lowercase names:

| Image | Required filename | Recommended format |
|---|---|---|
| Professional profile photograph | `prasad_natuskar.jpg` | Portrait, approximately 1200 × 1500 px |
| Miraya Business Hub | `miraya_business_hub.jpg` | Landscape, approximately 1600 × 1000 px |
| Konar Business Park | `konar_business_park.jpg` | Landscape, approximately 1600 × 1000 px |

Recommended image preparation:

- Use JPG or WebP-quality compression suitable for the web.
- Keep each image below approximately 500 KB where practical.
- Do not change the filenames unless the matching paths in `index.html` and `app.js` are also updated.
- Use a professional, well-lit head-and-shoulders portrait.
- Use high-resolution project photographs or authorised architectural renders.

No code changes are needed after files with the expected names are added.

## Contact form

The contact form uses EmailJS and requires an internet connection. Its configuration is located near the bottom of `app.js`:

```javascript
const EMAILJS_PUBLIC_KEY  = 'YOUR_PUBLIC_KEY';
const EMAILJS_SERVICE_ID  = 'YOUR_SERVICE_ID';
const EMAILJS_TEMPLATE_ID = 'YOUR_TEMPLATE_ID';
```

To configure it:

1. Create an account at [EmailJS](https://www.emailjs.com/).
2. Connect the email service that should receive website messages.
3. Create an email template.
4. Configure the template to accept these variables:
   - `from_name`
   - `from_email`
   - `subject`
   - `message`
   - `reply_to`
   - `to_name`
5. Copy the EmailJS public key, service ID, and template ID into `app.js`.
6. Restrict EmailJS requests to the final website domain in the EmailJS dashboard.
7. Test the form after deployment.

The public EmailJS key is designed for frontend use. Do not place private email-account passwords, server secrets, API secret keys, or login credentials in `app.js`.

## Main website behaviour

- Fixed responsive navigation
- Active navigation state while scrolling
- Mobile menu with outside-click and Escape-key closing
- Smooth anchor scrolling
- Reading-progress indicator
- Scroll-reveal animations
- Reduced-motion accessibility support
- Switchable project case studies
- Switchable skills categories
- Responsive experience timeline
- Dynamic footer year
- Contact-form status notifications
- Purpose-designed missing-image fallbacks

## Browser support

Use a current version of:

- Google Chrome
- Microsoft Edge
- Mozilla Firefox
- Apple Safari

JavaScript must be enabled for the project tabs, skills tabs, animations, mobile navigation, and contact form.

## Pre-publication checklist

- [ ] Add the professional profile photograph.
- [ ] Add both project images.
- [ ] Confirm permission to publish every photograph or render.
- [ ] Test every email, telephone, and LinkedIn link.
- [ ] Submit a test message through the contact form.
- [ ] Confirm all EmailJS domain restrictions.
- [ ] Check the website at mobile, tablet, laptop, and large-desktop widths.
- [ ] Verify all professional claims, dates, percentages, savings, qualifications, and project figures.
- [ ] Test keyboard navigation and visible focus states.
- [ ] Confirm the website works with reduced-motion enabled.
- [ ] Compress the final images.
- [ ] Add a favicon, canonical URL, and social-sharing image when the final domain is known.

## Deployment

This is a static website and can be hosted on GitHub Pages, Netlify, Vercel, Cloudflare Pages, or a conventional web server.

### GitHub Pages

1. Create a new GitHub repository.
2. Upload the project files while preserving the folder structure.
3. Open **Settings → Pages**.
4. Select **Deploy from a branch**.
5. Choose the `main` branch and `/ (root)` folder.
6. Save and wait for GitHub to publish the website.

### Netlify

1. Sign in to Netlify.
2. Choose **Add new site → Deploy manually**.
3. Drag the extracted portfolio folder into the upload area.
4. Open the generated website URL and test all functionality.

### Conventional hosting

Upload `index.html`, `styles.css`, `app.js`, and the `assets` folder to the public web root, commonly named `public_html`, `www`, or `htdocs`.

## Important privacy note

The website loads Google Fonts, the EmailJS browser library, and EmailJS functionality from external providers. Before publishing for a German or European audience, review the final hosting setup for GDPR requirements, including the privacy notice, external-resource handling, and contact-form data processing.

## Updating the website

- Edit page text and structure in `index.html`.
- Edit colours, spacing, layouts, animations, and responsive rules in `styles.css`.
- Edit project data, skills, navigation behaviour, and contact-form logic in `app.js`.
- Keep a backup before replacing published files.

After every update, refresh the browser without cache:

- Windows/Linux: `Ctrl + F5`
- macOS: `Command + Shift + R`

## Troubleshooting

### The website has no styling

Confirm that `styles.css` is in the same folder as `index.html` and retains the exact filename.

### Tabs or navigation do not work

Confirm that `app.js` is in the same folder as `index.html`, JavaScript is enabled, and the browser console shows no errors.

### Images show designed placeholders

This means the image files are missing, incorrectly named, or placed outside the `assets` folder. Check the exact filenames listed above.

### The contact form does not send

Check the EmailJS identifiers, template variables, allowed domain, email service connection, internet connection, and browser console.

### Recent changes do not appear

Perform a hard refresh or clear the browser cache. If the site is hosted, confirm that the updated files were uploaded to the correct directory.

---

© Prasad Natuskar. All professional information, project material, images, and contact details remain the responsibility of the portfolio owner.
