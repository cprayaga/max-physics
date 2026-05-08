# Max — Physics II Socratic Tutor

An AI-powered Socratic tutor for undergraduate Physics II (Electricity & Magnetism),
built for use with *University Physics with Modern Physics* by Young & Freedman, 15th edition.

Covers Chapters 21–32. Designed for a 6-week summer course.

---

## Features

- Socratic tutoring — Max guides students with questions, never gives away answers
- Full LaTeX math rendering (KaTeX)
- Math symbol toolbar for easy equation input
- Voice output (text-to-speech) and voice input (speech-to-text, Chrome only)
- Save & Pause — sessions saved to browser localStorage, resumable anytime
- Finish & Export — generates a timestamped PDF for Canvas submission
- Dark mode support

---

## Deployment (GitHub Pages — 5 minutes)

### Step 1 — Get an Anthropic API key
1. Go to [console.anthropic.com](https://console.anthropic.com)
2. Sign in or create an account
3. Go to **API Keys** and click **Create Key**
4. Copy the key (it starts with `sk-ant-...`)

### Step 2 — Add your API key to index.html
1. Open `index.html` in any text editor (Notepad, TextEdit, VS Code, etc.)
2. Find this line near the top of the `<script>` section:
   ```
   const API_KEY = 'YOUR_API_KEY_HERE';
   ```
3. Replace `YOUR_API_KEY_HERE` with your actual key, keeping the quotes:
   ```
   const API_KEY = 'sk-ant-api03-...';
   ```
4. Save the file.

### Step 3 — Create a GitHub repository
1. Go to [github.com](https://github.com) and sign in (or create a free account)
2. Click the **+** button → **New repository**
3. Name it `max-physics` (or anything you like)
4. Set it to **Public**
5. Click **Create repository**

### Step 4 — Upload the file
1. On the repository page, click **uploading an existing file**
2. Drag `index.html` into the upload area
3. Also drag `README.md` if you'd like
4. Click **Commit changes**

### Step 5 — Enable GitHub Pages
1. Go to your repository **Settings** tab
2. Click **Pages** in the left sidebar
3. Under **Source**, select **Deploy from a branch**
4. Under **Branch**, select `main` and folder `/ (root)`
5. Click **Save**
6. Wait about 60 seconds, then refresh the page
7. You will see: *"Your site is live at https://yourusername.github.io/max-physics/"*

### Step 6 — Share with students
Copy the URL and post it on Canvas. Tell students:
- Use **Chrome** for the best experience (voice features require Chrome)
- Do **not** use Incognito mode (sessions won't save)
- Enter their name, student ID, and course section on the welcome screen
- Select their chapter and start chatting with Max

---

## Canvas Setup

Create the following folder structure in your Canvas course Files:

```
Max Sessions/
  Ch 21 — Electric Charge/
  Ch 22 — Electric Field/
  Ch 23 — Electric Potential/
  Ch 24 — Capacitance/
  Ch 25 — Current & EMF/
  Ch 26 — DC Circuits/
  Ch 27 — Magnetic Forces/
  Ch 28 — Magnetic Sources/
  Ch 29 — Induction/
  Ch 30 — Inductance/
  Ch 31 — AC Circuits/
  Ch 32 — EM Waves/
```

Students download their session PDF and upload it to the correct chapter folder.
The PDF filename is auto-generated as:
`Max_Session_Ch21_Jane_Smith_2026-05-08.pdf`

---

## Grading

Suggested weighting (20% of total course grade):
- Minimum exchanges per session: recommend 8–10 for full credit
- Session timestamp is embedded in the PDF
- Duration is tracked and included in the PDF

---

## Security Note

The API key is visible in the HTML source. For a small class this is generally
acceptable — usage is low and you can set spending limits in the Anthropic Console.
For a larger deployment, ask your ITS department to set up a simple backend proxy
that keeps the key server-side.

---

## Suggested Syllabus Language

> **Max AI Tutoring Sessions (20% of grade)**
> After each class, you are encouraged to open a session with Max, our AI Physics
> tutor, at [URL]. Max will help you work through concepts and problems using the
> Socratic method — he asks questions rather than giving answers, so come prepared
> to think! Sessions should be started within 24 hours of each lecture for maximum
> benefit. You may complete a session in multiple sittings using the Save & Pause
> feature. When finished, click Finish & Export and upload your PDF to the correct
> Canvas folder under Max Sessions. Use Chrome. Do not use Incognito mode.

---

Built with Claude · KaTeX · jsPDF · Tabler Icons
