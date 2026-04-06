# Kinetic Landing Page

Pre-launch countdown page for **Kinetic** by Nanobubble Technologies Ltd.  
Designed for QR code scanning at Interclean Amsterdam 2026.

## Deploy to Vercel

### Option 1: Vercel CLI
```bash
npm i -g vercel
cd kinetic-landing
vercel
```

### Option 2: GitHub
1. Push this folder to a GitHub repo
2. Import the repo at [vercel.com/new](https://vercel.com/new)
3. Vercel auto-detects the static site. Deploy.

### Option 3: Drag and drop
Go to [vercel.com/new](https://vercel.com/new) and drag this folder in.

## Custom domain

After deploying, add your domain in Vercel project settings:
- `kinetic.water` / `kineticwater.co.uk` / etc.
- Vercel provides free SSL

## Email collection

The notify button is client-side only (placeholder). To collect emails:

1. **Formspree** (quickest): Sign up at formspree.io, get a form ID, replace the TODO in `index.html`:
   ```js
   fetch('https://formspree.io/f/YOUR_FORM_ID', {
     method: 'POST',
     headers: { 'Content-Type': 'application/json' },
     body: JSON.stringify({ email: input.value })
   })
   ```

2. **Vercel serverless function**: Add an `api/notify.js` file for server-side handling.

## Font swap

The page uses Google Fonts (Bebas Neue + Outfit) as stand-ins.  
For production, replace with self-hosted Technica Bold and DIN Next LT Pro:
- Update the `@font-face` declarations
- Swap font-family values marked with comments in the CSS

## Files

```
index.html    - Single-file landing page (HTML + CSS + JS inline)
vercel.json   - Vercel routing and security headers
README.md     - This file
```
