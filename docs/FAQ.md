# ❓ Cyber Playbook FAQ – Hocking College Edition

This FAQ covers the most common issues students hit while building and maintaining their Cyber Playbook.  
Follow this guide and you’ll avoid 99% of problems.

---

## 🧱 Basic Site Questions

### 💡 What is this site?
Your **Cyber Playbook** is a public, professional portfolio of your hands-on labs.  
You add “Topic” blocks (labs/projects) to `index.html` under three subjects: **Hardware**, **Networking**, and **Security**.  
The site is hosted on **GitHub Pages** so you can share it with instructors and employers.

### 🌐 What’s my site link?
After enabling GitHub Pages, your URL is:

https://<your-username>.github.io/<your-repo-name>/

makefile
Copy code

**Example:**

https://claytonholden.github.io/Cyber-playbook2/

markdown
Copy code

### 🧑‍💻 What files am I allowed to edit?
- **Edit:** `index.html`, and add screenshots to `assets/images/`.
- **Leave alone (unless you know what you’re doing):** `assets/styles.css`, everything in `docs/` and `templates/`.

---

## 🧩 Topic & Editing Issues

### How do I add a new Topic?
1. Open `templates/topic-block.html`
2. Click **Raw** → Select All → Copy.
3. Open `index.html` → **Edit** → scroll to the correct **Subject** section:
   - `<section id="hardware" class="subject">`
   - `<section id="networking" class="subject">`
   - `<section id="security" class="subject">`
4. Paste the copied Topic **under the last** `<section class="topic">…</section>` in that subject.
5. Fill in **Overview**, **Approach**, **Evidence**, **Reflection** and update screenshot links.

> Detailed steps are in `docs/HTML_EDITING.md`.

### ❌ My page shows raw HTML or the layout looks broken.
You probably missed a closing tag (`</section>` or `</div>`) or pasted a Topic outside the subject.

**Fix:**
- Copy a fresh block from `templates/topic-block.html`.
- Paste it inside the correct subject section.
- Ensure all tags close properly.

### 🖼 My images don’t display (404 Not Found).
- Upload screenshots into **`assets/images/`** (lowercase path).
- Use **lowercase, hyphenated** filenames (case-sensitive on the web), e.g.:

2025-11-windows-install-01.png
2025-11-windows-install-02.png

php-template
Copy code

- Link them in your Topic’s Evidence list, e.g.:

```html
<ul class="evidence">
  <li><a href="assets/images/2025-11-windows-install-01.png" target="_blank">System Properties</a></li>
  <li><a href="assets/images/2025-11-windows-install-02.png" target="_blank">IP Config</a></li>
</ul>
🎨 My colors or icons look off.
You can safely customize accent color, icons (emoji), corner radius, and optionally font.
See docs/THEME.md for exact steps.

⚙️ The sidebar/top bar/header disappeared.
A structural tag like <header> or <aside> may have been removed or a section didn’t close.

Fix: Revert to a known-good version:

Open index.html → History

Click the last working commit

Choose Revert

🖥 GitHub Pages & Repository Problems
🕓 My site hasn’t updated.
Wait 1–2 minutes; Pages rebuilds automatically after each commit.

Hard refresh your browser (Ctrl/Cmd + Shift + R).

🚫 My site says “404 Not Found.”
Check Pages is enabled:

Settings → Pages → Build and deployment

Source = Deploy from a branch

Branch = main, Folder = / (root)

If it’s already set, wait a minute and refresh—your last build may still be processing.

🧭 I can’t find my images folder.
It should be at assets/images/.
If it’s missing, create it with that exact lowercase path and re-upload images.

🔄 I made a mistake and pushed it.
No problem—use file history:

Open the file → History → click the last good version → Revert.

📄 Submissions & Grading
📦 What do I turn in for class?
Your live Pages URL (primary deliverable).

If your instructor asks: a PDF export of the page (Print → Save as PDF).

Ensure your latest Topic is visible and links work.

🧾 What will be graded?
Correct Topic structure (Overview / Approach / Evidence / Reflection).

1–3 working screenshots linked in Evidence.

Clear, original Reflection (not copied from lab text).

Professional filenames (lowercase, hyphenated).

🎨 Customization & Personality
💅 How do I change colors?
Open assets/styles.css, find the variables:

css
Copy code
:root{
  --bg:#0b0d10;
  --panel:#0f1319;
  --ink:#e8edf3;
  --muted:#a7b3c2;
  --line:#1f2630;
  --accent:#63e0ff; /* change this for link/button color */
  --radius:16px;
}
Change --accent: to a new hex:

Pink: #ff7ab6

Green: #00d27a

Orange: #ff9a3c

Sky Blue: #00a8ff

🧠 Can I change icons?
Yes. In index.html, each subject has an emoji in the title, e.g.:

html
Copy code
<h2 class="subject-title"><span class="icon">🧩</span> Hardware</h2>
Swap the emoji with: 🧰 🔧 🖥️ 🌐 🔐 ⚙️ 🛰️ 🧠

🖋 Can I use a different font?
Add this line inside <head> in index.html (above your stylesheet):

html
Copy code
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap" rel="stylesheet">
Then in assets/styles.css, change the base font to use Inter.

🧯 Emergencies
😭 I broke everything.
Go to index.html → History

Find the last working version

Click Revert

Reapply your Topic using the template block carefully

🔒 I deleted files or folders.
Check the repo commits and browse files from older commits to restore.

If needed, re-copy missing folders from the original template.

🧩 Still Need Help?
Before asking:

Read this FAQ fully

Review docs/HTML_EDITING.md

Check your site’s History

Revert if you made a major error

If it’s still broken, send your instructor:

A link to your repo

A link to your live site

A screenshot of the issue

makefile
Copy code
::contentReference[oaicite:0]{index=0}
