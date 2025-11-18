## 🎯 What this is
- A clean, scrollable website (GitHub Pages) that shows **what you built**, **how you built it**, and **evidence**.
- A light structure that teaches real Git/GitHub skills without heavy tooling.
- A template you can customize visually while keeping consistent content standards.

## 💡 Why use this
- **Employers want proof**: screenshots + concise write-ups beat a resume bullet.
- **Instructors grade faster**: every Topic uses the same 4-part block.
- **Students learn Git**: practical commits, pushes, and PRs (or the web editor).

---

## 🧭 How to use this effectively
- **One Topic = One lab** (don’t combine multiple labs in one Topic).
- Fill out the **4 parts** every time:
  1) **Overview** (what/why)  
  2) **Approach** (steps/commands/tools)  
  3) **Evidence** (1–3 screenshots in `assets/images/`)  
  4) **Reflection** (what worked, what you learned, what you’d improve)
- Name screenshots clearly: `YYYY-MM-labname-01.png`.
- Keep filenames lowercase (Linux hosting is case-sensitive).

---

## 🪜 Quick Start

### Option A — GitHub (no terminal)
1. Open your repo → **Settings → Pages** → Deploy from branch = `main` / root.
2. In the repo, click **Add file → Create new file** to upload screenshots to `assets/images/`.
3. Click **index.html → Edit**.
4. Scroll to the correct **Subject** and paste a copy of the template from `templates/topic-block.html`.
5. Fill in your content, link your images, **Commit**.

### Option B — Command line
```bash
git clone https://github.com/<you>/Cyber-playbook2.git
cd Cyber-playbook2
# edit index.html, add images to assets/images/
