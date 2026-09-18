# Yusuf & Sana — Nikah Invitation

A single-page Islamic wedding invitation. Plain HTML/CSS/JS — no build step, no framework.

## Files
- `index.html` — the whole site (structure + styles + script)
- `audio/nasheed.mp3` — **you need to add this file yourself.** Drop any royalty-free/permitted nasheed MP3 here with this exact filename, or update the `<source src="...">` path in `index.html` to match your file. I can't legally source or embed a copyrighted nasheed track for you.
- `images/` — empty folder, ready if you want to add photos later.

## What to edit before sending it out
Open `index.html` and update:
1. **Names & parents** — currently placeholder ("Mohammed Yusuf Rahman" / "Sana Fathima") in the hero section and the "Cordial Invitation" card. Search for these names and replace.
2. **Date/time/venue** — currently 15 Oct 2026, 11:30 AM, Unity Hall, Kallapu, Mangaluru. The countdown timer's target date is set in the `<script>` tag: `new Date("2026-10-15T11:30:00+05:30")` — update this if the date/time changes, in Indian Standard Time (+05:30) format.
3. **Map** — the embedded map and "Get Directions" link both search for "Unity Hall, Kallapu, Mangaluru, Karnataka". If the exact spot doesn't come up correctly on Google Maps, replace it with the venue's real Google Maps link/coordinates.
4. **Nasheed audio** — add your MP3 file as described above.

## Deploy to Vercel
**Option A — no coding tools, fastest:**
1. Go to [vercel.com](https://vercel.com) and sign up/log in.
2. Click **Add New → Project → Deploy without Git** (or drag-and-drop).
3. Drag this whole folder (with `index.html` and `audio/`) into the upload area.
4. Click **Deploy**. Vercel will give you a live `.vercel.app` link in under a minute.

**Option B — via GitHub (recommended if you'll keep editing):**
1. Create a new GitHub repo and push this folder to it.
2. On [vercel.com](https://vercel.com), click **Add New → Project**, then import that GitHub repo.
3. Leave all settings as default (it's a static site — no framework, no build command needed).
4. Click **Deploy**.

**Option C — via Vercel CLI:**
```bash
npm i -g vercel
cd wedding-invite
vercel
```
Follow the prompts; it deploys straight from your terminal.

Once deployed, you can add a custom domain or a nicer subdomain from the Vercel project settings.
