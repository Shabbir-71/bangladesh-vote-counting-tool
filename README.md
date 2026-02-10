# Vote Counting Tool for Bangladesh Election

A static, responsive web app that replicates the official vote counting form (Form 16 style) for Bangladesh National Parliament elections. It supports English and Bangla (BN) with a single toggle and works offline after first load.

## Features

- **Header**: Election Commission logo, title, and EN/BN language toggle
- **Form fields**: Electoral area, polling center, total voter count
- **Vote table**: Add rows (ক্রমিক ১, ২, … / Serial 1, 2, …), candidate name, symbol, valid votes, challenged valid votes, auto total per row (figures + words)
- **+ / −** inside Valid Votes and Challenged Valid Votes (and for invalid votes below)
- **Grand total** row (মোট) and three summary fields with live calculations
- **Responsive**: Usable on mobile and tablet; table scrolls horizontally when needed

## Hosting on GitHub Pages (detailed steps)

Follow these steps to put your Vote Counting Tool online for free using GitHub Pages.

---

### Step 1: Create a GitHub account (if you don’t have one)

1. Go to [https://github.com](https://github.com).
2. Click **Sign up** and complete registration.
3. Verify your email if asked.

---

### Step 2: Create a new repository

1. Log in to GitHub.
2. Click the **+** icon (top right) → **New repository**.
3. Fill in:
   - **Repository name**: e.g. `bangladesh-vote-counting` or `vote-counting-tool` (no spaces).
   - **Description** (optional): e.g. “Vote counting tool for Bangladesh election”.
   - **Public**.
   - Do **not** check “Add a README file” (you already have files to upload).
4. Click **Create repository**.

---

### Step 3: Upload your files to the repository

You need these files in the **root** of the repo (not inside any folder):

- `index.html` — required  
- `election_commission_logo.jpg` — required (logo in header)

**You do not need to install Git.** Use **Option A** below (upload in the browser). Option B is only if you want to use the command line and have Git installed.

---

**Option A — Upload in the browser (recommended, no Git needed)**

1. On the new repo page, click **uploading an existing file** (or **Add file** → **Upload files**).
2. Drag and drop `index.html` and `election_commission_logo.jpg` from your project folder into the browser, or click **choose your files** and select them.
3. In the “Commit message” box, type e.g. `Add vote counting tool`.
4. Click **Commit changes**.

Your files are now on GitHub. Continue with **Step 4** below.

---

**Option B — Upload using Git (only if Git is installed)**

The commands below are meant to be typed (or pasted) **one by one** into a terminal (Command Prompt or PowerShell), **not** including the word `bash` or the triple backticks. Those are just formatting in the README.

1. Open **Command Prompt** or **PowerShell**: press `Win + R`, type `cmd` or `powershell`, press Enter.
2. Go to your project folder, e.g.  
   `cd "E:\My Projects\Bangladesh Election Voting Count Website"`
3. Run these commands **one at a time** (replace YOUR_USERNAME and YOUR_REPO_NAME):

   `git init`  
   `git add index.html election_commission_logo.jpg`  
   `git commit -m "Add vote counting tool"`  
   `git branch -M main`  
   `git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git`  
   `git push -u origin main`

   If Git asks for login, use a [Personal Access Token](https://github.com/settings/tokens) instead of your password.

If you see **“git is not recognised”**, Git is not installed. Use **Option A** (browser upload) instead, or install Git using the steps in **“Installing Git on Windows”** below.

---

### Step 4: Turn on GitHub Pages

1. In your repository on GitHub, click **Settings** (top menu of the repo).
2. In the left sidebar, under **“Code and automation”**, click **Pages**.
3. Under **“Build and deployment”**:
   - **Source**: select **Deploy from a branch**.
   - **Branch**: choose **main** (or **master** if that’s your default branch).
   - **Folder**: choose **/ (root)**.
4. Click **Save**.

---

### Step 5: Get your live URL and check the site

1. After saving, GitHub will build and deploy the site (usually within 1–2 minutes).
2. At the top of the **Settings → Pages** section you’ll see a message like:  
   **“Your site is live at `https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/`”**
3. Click that link or open it in a new tab.
4. You should see the Vote Counting Tool with the logo. If the logo is missing, confirm `election_commission_logo.jpg` is in the same repo root as `index.html`.

---

### Step 6: Updating the site later

- **If you used the browser upload**: upload the new `index.html` (or logo) again via **Add file** → **Upload files**, then commit. The site will update in a couple of minutes.
- **If you used Git**: edit locally, then in a terminal (in your project folder) run:  
  `git add .`  
  `git commit -m "Update vote counting tool"`  
  `git push`

---

### Installing Git on Windows (optional)

You only need Git if you want to use **Option B** (command-line upload). For hosting this page, **Option A (browser upload) is enough** and does not require Git.

If you do want to install Git on Windows:

1. **Download Git for Windows**
   - Go to [https://git-scm.com/download/win](https://git-scm.com/download/win).
   - The download should start automatically (64-bit or 32-bit depending on your PC).

2. **Run the installer**
   - Double-click the downloaded file (e.g. `Git-2.43.0-64-bit.exe`).
   - Click **Next** through the steps. The default options are fine.
   - When asked “Adjusting your PATH environment”, keep **“Git from the command line and also from 3rd-party software”**.
   - Click **Next** until **Install**, then finish.

3. **Use Git**
   - **Close any open Command Prompt or PowerShell windows**, then open a **new** one (so it picks up the updated PATH).
   - Type `git --version` and press Enter. You should see something like `git version 2.43.0`. If you see that, Git is installed.

4. **About “```bash”**
   - In this README, ` ```bash ` is **not** a command. It is just markdown for “the following lines are terminal commands”.
   - You only type or paste the **actual commands** (e.g. `git init`, `git add index.html`), each on its own line, and never type `bash` or the backticks.

---

### Summary

| What            | Value                                                                 |
|-----------------|-----------------------------------------------------------------------|
| **Live URL**    | `https://<your-username>.github.io/<repo-name>/`                       |
| **Required files** | `index.html`, `election_commission_logo.jpg` in the repo root    |
| **Build**       | None — GitHub serves the files as-is.                                |

No server or build step is needed; the page runs entirely in the browser.

## Files

| File | Purpose |
|------|--------|
| `index.html` | Single-page app (HTML, CSS, JS). All logic and styles are inside this file. |
| `election_commission_logo.jpg` | Logo shown in the header. Must be in the same folder as `index.html`. |

## Browser support

Works in modern browsers (Chrome, Firefox, Safari, Edge) with JavaScript enabled.
