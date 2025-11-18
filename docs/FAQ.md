# ❓ Cyber Playbook — FAQ and Self-Help Guide

This FAQ answers the most common questions about creating, updating, and maintaining your Cyber Playbook.

---

## ⚙️ 1  General Site Behavior

### 🧱 My page shows raw HTML text instead of a web page.
You probably pasted a Topic outside the subject container or missed a closing `</section>` or `<div>`.  
Fix → Copy a fresh block from `templates/topic-block.html`, paste it correctly, and ensure every opening tag has a matching close.

### 🖼️ My images don’t load (404 error).
- File must exist in `assets/images/`.
- Filenames are case-sensitive → use lowercase only.
- Link using a relative path, for example:
assets/images/2025-12-server-01.png

bash
Copy code

### 🎨 My colors look off or the theme is broken.
The CSS file might have been renamed or moved.  
Restore the line in `<head>`:
```html
<link rel="stylesheet" href="assets/styles.css">
🔗 The sidebar links don’t highlight when scrolling.
Make sure each subject section keeps the correct ID:

python
Copy code
<section id="hardware" class="subject">
<section id="networking" class="subject">
<section id="security" class="subject">
🧩 2 Editing and Structure
🪜 Where do I paste new Topics?
Inside the subject you’re working on.
Scroll to the end of that section in index.html and paste below the last </section> that has class topic.

🧱 How do I upload screenshots?
Add file → Upload files → target folder assets/images/.
Use names like 2025-12-firewall-lab-01.png.

🪄 Can I edit entirely on GitHub without VS Code?
Yes. All changes can be made in the web editor and committed directly.

🔁 How do I revert if I break something?
index.html → History → Revert this commit to restore the last working version.

🧱 Can I add a new Subject (e.g., Cloud or Scripting)?
Yes → duplicate a subject block (section id="...") and add its link to the sidebar.

💡 3 Customization and Style
🎨 How do I change the accent color?
Open assets/styles.css and edit:

css
Copy code
:root{
  --accent:#63e0ff; /* change this value */
}
Use any HEX color code.

🔠 Can I use a different font?
Add to the <head> of index.html:

html
Copy code
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap" rel="stylesheet">
Then edit the font line in CSS to use Inter.

🔧 Can I add my own emoji icons for subjects?
Yes. Find the subject title and replace the emoji inside:

html
Copy code
<h2 class="subject-title"><span class="icon">🧩</span> Hardware</h2>
🧠 4 GitHub Pages and Deployment
🌐 My site URL is 404 or not updating.
Enable Pages: Settings → Pages → Deploy from branch (main / root).
Wait ~1-2 minutes for the build.

🕒 I updated files but nothing changed.
Hard refresh (Windows Ctrl + Shift + R / Mac Cmd + Shift + R).
Sometimes Pages cache takes a minute to update.

📄 How do I export for LMS submission?
Open your live page → Print → “Save as PDF”.

🧰 5 Advanced and Troubleshooting
🪵 How do I view the site locally before committing?
You can’t run Jekyll on the college machines easily, but you can preview by opening index.html in a browser locally (it will still render).

🧾 How do I check what’s changed?
git status shows new or modified files.
git log shows commit history.

🧼 Can I clean out old labs?
Yes → delete that Topic block from index.html and remove its screenshots from assets/images/.

🧱 6 Rules Recap (Do Not Break)
Don’t delete index.html, assets/, templates/, or docs/.

Always copy the Topic template — never hand-type new sections.

Keep filenames lowercase.

If it breaks → use History → Revert.

Check your site link after every lab.

