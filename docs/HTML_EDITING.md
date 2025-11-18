# ✏️ Exact Guide: Editing `index.html` (Safely)

This is the **step-by-step guide** for adding new Topics to your Cyber Playbook.  
If you follow this exactly, you will not break the site.

---

## 🧱 1. How Your Page Is Structured

Your site (`index.html`) has three main **Subjects**:
- `<section id="hardware" class="subject">`
- `<section id="networking" class="subject">`
- `<section id="security" class="subject">`

Inside each subject are multiple `<section class="topic">` blocks — **one per lab**.

---

## 🪜 2. Add a New Topic (the Safe Way)

1. **Open the Template**
   - Go to `templates/topic-block.html`
   - Click **Raw** → Select All → Copy

2. **Paste It Into `index.html`**
   - Open `index.html` → click **Edit**
   - Scroll to your Subject (Hardware / Networking / Security)
   - Paste the block **below the last `<section class="topic">…</section>`**

3. **Fill in Your Content**
   - Edit the `<h3>` with your Topic name.
   - Fill in `<p>` and `<ul>` sections for Overview, Approach, Reflection.
   - Link screenshots in the Evidence section.

Example:
```html
<ul class="evidence">
  <li><a href="assets/images/2025-12-server-01.png" target="_blank">System Properties</a></li>
  <li><a href="assets/images/2025-12-server-02.png" target="_blank">Server Manager</a></li>
</ul>

🖼️ 3. Uploading and Linking Screenshots

Click Add file → Upload files

Upload images into assets/images/

Use lowercase, hyphenated filenames:

2025-12-windows-install-01.png
2025-12-windows-install-02.png


Link those files in your Evidence list.

🧪 4. Test Before Committing

Scroll down and confirm your Topic shows in the right Subject.

Click each Evidence link — should open the image (no 404).

Check that text formatting matches other Topics.

🧠 5. Common Mistakes (and Fixes)
Problem	Cause	Fix
Page shows raw HTML text	Missing closing </section> or <div>	Copy a fresh block and ensure all tags close
Screenshot 404	Wrong folder or filename case	File must exist in assets/images/ using exact lowercase name
Styles missing	CSS link removed from <head>	Restore <link rel="stylesheet" href="assets/styles.css">
Topic outside Subject	Pasted block in wrong spot	Always paste inside `<section id="hardware
🧯 6. If You Break the Page

Go to index.html → History

Click the last good commit

Choose Revert this commit

Reapply your changes carefully using the template block

✅ 7. Golden Rules

Always copy from templates/topic-block.html — never free-type new sections.

Never delete <section id="…"> lines.

Keep one empty line between Topics.

Preview visually before submitting your link.

