# How to Update Your Website (App + Website in One Repo)

Since you are using one repository for both your **App Code** and **Website**, and you already have files on GitHub, follow these steps to add the website without messing up your app.

## Step 1: Prepare the "docs" folder
I have already renamed your `website` folder to `docs`. This is special. GitHub Pages loves the `docs` folder. It allows you to keep your main app code in the root, and just the website files in `docs`.

## Step 2: Open Terminal
1.  Open Command Prompt or PowerShell.
2.  Navigate to your project folder:
    ```powershell
    cd e:\journal
    ```

## Step 3: Link and Push (If you haven't locally)
**Important:** If you see "fatal: not a git repository" when you run git commands, it means your computer doesn't know about the GitHub files yet.

Run these exact commands to connect everything:

```powershell
# 1. Initialize Git locally
git init

# 2. Add ONLY the website files (Ignore the App for now)
git add docs

# 3. Commit the changes
git commit -m "Add website files"

# 4. Link to your GitHub (Skip if already linked)
# Replace [YOUR_URL] with your actual GitHub URL
git remote add origin [YOUR_URL]
# Example: git remote add origin https://github.com/devworkscribe/workscribe.git

# 5. Push to GitHub
# If you get an error saying "updates were rejected", run: git pull origin main --allow-unrelated-histories
git push -u origin main
```

## Step 4: Turn on the Website (The Magic Step)
1.  Go to your repository on GitHub.com (`https://github.com/devworkscribe/workscribe`).
2.  Click **Settings** (top right tab).
3.  Click **Pages** (left sidebar).
4.  Under **Build and deployment**:
    *   **Source:** Deploy from a branch
    *   **Branch:** Select `main` (or master).
    *   **Folder:** Select `/docs` (Change this from /(root) to /docs).
5.  Click **Save**.

## Done!
Your website will be live at: `https://devworkscribe.github.io/workscribe/`

## How to Update the Website later
Whenever you edit files in the `docs` folder (like changing text in index.html):

```powershell
git add docs
git commit -m "Update website text"
git push
```
