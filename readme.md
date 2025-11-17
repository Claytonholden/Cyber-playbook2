# Cyber Playbook — Getting Started

This playbook is a single, scrolling page that’s easy to update in the GitHub website.  
Each topic lives as a block on `index.html` with **Overview → Approach → Evidence → Reflection**.

---

## 1) Setup & Publish

**Fork** or create your own repo named `Cyber-Playbook`.  
Add these files:
- `index.html` (main page)
- `assets/style.css`
- `README.md`
- Optional: `files/Resume.pdf`, `assets/images/`

**Enable Pages:**  
Settings → Pages → Build & Deployment  
- Source: **Deploy from a branch**  
- Branch: `main`  
- Folder: `/ (root)` → **Save**

Site URL:  https://<your-username>.github.io/Cyber-Playbook/


---

## 2) Submitting Work (what to submit)

- Update `index.html` with a new **Topic** under the correct **Subject** (Hardware / Networking / Security).
- Include:
  - **Overview** (what/why)
  - **Approach** (key steps/commands)
  - **Evidence** (1–3 screenshots in `assets/images/`)
  - **Reflection** (2–4 sentences)
- Share:
  - Your **live Pages URL**
  - Any required files (PDF/ZIP) in `files/`

> **Naming screenshots**: `2025-11-lab2-01.png`, `2025-11-iam-01.png` (keeps things tidy)

---

## 3) Add a Topic (web UI)

1. Go to `index.html` → **Edit**  
2. Duplicate a `&lt;section class="topic"&gt;…&lt;/section&gt;` block and paste it under the right subject.  
3. Change the title and text.  
4. Upload screenshots: Go to `assets/images/` → **Add file** → **Upload files**.  
5. Link screenshots in your topic as:assets/images/2025-11-lab2-01.png

6. **Commit changes** → wait ~60s → refresh your site.

---

## 4) Optional: Work via Command Line

```bash
# clone
git clone https://github.com/<your-username>/Cyber-Playbook.git
cd Cyber-Playbook

# create a branch per lab (recommended)
git checkout -b yourname-weekNN

# edit files, add screenshots to assets/images/
git add .
git commit -m "Week NN: <Topic Title>"
git push -u origin yourname-weekNN

# open a Pull Request to main (if your instructor wants PRs)

## Turn-in checklist (students)
- Add exactly one new **Topic** under Hardware/Networking/Security.
- Include **Overview → Approach → Evidence → Reflection**.
- Upload **1–3 screenshots** to `assets/images/` and link them.
- Share the **live Pages URL** and (if required) a PDF export.
- Keep filenames tidy: `YYYY-MM-topic-##.png`.

