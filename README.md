# Dave's Hand — Deploy Guide

Your booking page is in this folder: `index.html` + the `assets` images.
Do two things: (A) turn on form emails, then (B) deploy to Vercel.

---

## A. Turn on form-to-email (Formspree) — 5 minutes

Right now the form shows clients your pricing but doesn't email you yet.
Fix that:

1. Go to **formspree.io** and sign up free (use your business email).
2. Click **+ New Form**. Name it "Dave's Hand Inquiries".
   Set the notification email to the inbox where you want inquiries.
3. Copy the form's **endpoint URL** — it looks like:
   `https://formspree.io/f/abcdwxyz`
4. Open `index.html` in any text editor. Near the bottom, find this line:
   ```
   var FORMSPREE_ENDPOINT = "https://formspree.io/f/YOUR_FORM_ID";
   ```
   Replace the URL with **your** endpoint. Save the file.
5. The first time a real person submits, Formspree emails you once to
   confirm the form — click the link and you're done. Every inquiry
   after that lands in your inbox, fully filled out.

Free plan = 50 submissions/month. Plenty to start.

---

## B. Deploy to Vercel (free, live URL, no domain needed)

You get a free address like `daves-hand.vercel.app` immediately.

### Easiest: Vercel CLI
1. Install **Node.js** from nodejs.org (if you don't have it).
2. Open a terminal **inside this folder**.
3. Run:  `npm i -g vercel`
4. Run:  `vercel`  → log in, press Enter to accept the defaults.
   It deploys and gives you a live preview link.
5. Run:  `vercel --prod`  → gives you the final public link to share.

### No-terminal alternative: GitHub + Vercel
1. Create a free GitHub account, make a new repository,
   and upload these files (`index.html` + the `assets` folder).
2. On **vercel.com**, click **Add New → Project**, import that repo,
   and click **Deploy**. Done.

Start sending the `.vercel.app` link to inquirers right away.

---

## C. Add your own domain (later, optional)

1. Buy a domain (Namecheap, GoDaddy, or a local PH registrar) —
   e.g. `daveshand.com`. Usually ₱500–1,000/year.
2. In your Vercel project → **Settings → Domains → Add**.
3. Follow Vercel's DNS instructions (copy the records into your
   domain registrar). It connects in a few minutes to a few hours.

Nothing breaks — your site just becomes reachable at the new address too.

---

*Need help on any step? Just tell me where you're stuck.*
