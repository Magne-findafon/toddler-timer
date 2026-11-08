# Publishing Toddler Timer (free)

The whole site is **one file: `index.html`**. No build step, no server code.
That makes it free to host forever.

**Recommendation: GitHub Pages.** It's free, has no bandwidth worries at this
size, gives you HTTPS, and keeps a history of every change. You can do it all
in the web browser. You don't need the terminal.

Cost: **0 kr.** The only optional cost is your own domain name (about
100–150 kr/year), which you can add later.

---

## Option A: GitHub Pages (recommended)

### 1. Create a GitHub account
1. Go to <https://github.com/signup> and sign up (free plan).
2. Your username becomes part of the address, for example
   `https://YOURNAME.github.io/toddler-timer/`.

### 2. Create the repository
1. Once logged in, click the **+** in the top right corner, then **New repository**.
2. **Repository name:** `toddler-timer`
3. Choose **Public**. Free GitHub Pages requires a public repo.
4. Leave everything else as is and click **Create repository**.

### 3. Upload the file
1. On the new, empty repo page, click the link **"uploading an existing file"**.
2. Drag `index.html` from this folder into the browser window.
   (You can also drag `PUBLISHING.md` and `BRIEFTottlertimer.md` if you want them stored there too.)
3. At the bottom, click **Commit changes**.

### 4. Turn on GitHub Pages
1. In the repo, go to **Settings**, then **Pages** (in the left menu).
2. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
3. Set **Branch** to `main` and the folder to `/ (root)`, then click **Save**.
4. Wait 1–2 minutes and refresh the page. A box appears at the top saying
   **"Your site is live at https://YOURNAME.github.io/toddler-timer/"**.

### 5. Updating later
Open `index.html` in the repo, click the pencil icon to edit, or use
**Add file**, then **Upload files**, to replace it with a new version. Click
**Commit changes**. The site updates within a minute or two.

### 6. (Optional) Your own domain
In **Settings**, then **Pages**, under **Custom domain**, enter for example
`timer.yourdomain.no` and follow the DNS instructions GitHub shows. Then tick
**Enforce HTTPS**.

---

## Option B: Netlify Drop (fastest, no repo)
If you just want it online in 30 seconds:
1. Go to <https://app.netlify.com/drop>.
2. Drag **this whole folder** onto the page.
3. You get a live URL immediately. Create a free account to keep it permanently.

This is quicker, but you don't get version history, and updating means
dragging the folder in again.

---

## After publishing: test on real devices
The brief's checklist can only be fully verified on real devices:
- [ ] iPhone Safari: start a timer, lock the phone, unlock it. The bar should have moved the right amount.
- [ ] iPhone: turn on "Soft chime", run a 1-minute timer with the screen on. The chime should play at the end.
- [ ] Run a 30-minute timer and confirm the screen stays on (Screen Wake Lock: iOS 16.4+, Android Chrome).
- [ ] Android Chrome, iPad, and desktop Chrome/Firefox/Safari: rotate and resize, the bar should adapt.

Tip for parents: on iPhone, **Share, then Add to Home Screen** makes it open
like a calm, full-screen object with no browser bars.
