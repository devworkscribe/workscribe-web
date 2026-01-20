# Hosting Your Website for Free

You can host these files for free using **GitHub Pages** (recommended) or Netlify.

## Option 1: GitHub Pages (Easiest)

1.  Create a new public repository on GitHub (e.g., `workscribe-website`).
2.  Upload the files in this folder (`index.html`, `style.css`, `privacy.html`) to that repository.
3.  Go to **Settings** > **Pages**.
4.  Under **Source**, select `Deploy from a branch` and choose `main` / `root`.
5.  Your site will be live at `https://yourusername.github.io/workscribe-website/`.
6.  Use this URL in your Play Store listing.

## Option 2: Netlify (Drag & Drop)

1.  Go to [Netlify Drop](https://app.netlify.com/drop).
2.  Drag and drop the `website` folder onto the page.
3.  It will instantly publish your site and give you a URL (e.g., `https://funny-name-1234.netlify.app`).
4.  You can change the site name in "Site Settings".

## Option 3: Firebase Hosting (Google's Static Hosting) - Recommended for "Google" ecosystem

If you prefer a Google service, **Firebase Hosting** is the best way to host these raw HTML/CSS files. It is free and professional.

1.  Go to the [Firebase Console](https://console.firebase.google.com/) and create a new project.
2.  Install the Firebase CLI tools on your computer (`npm install -g firebase-tools`).
3.  Open a terminal in this `website` folder.
4.  Run `firebase login`.
5.  Run `firebase init hosting`.
    *   Select your project.
    *   Type `.` (current directory) as your public directory.
    *   Type `N` for single-page app rewrites.
6.  Run `firebase deploy`.
7.  Your site will be live at `https://your-project-id.web.app`.

## Option 4: Google Sites (Drag & Drop Builder)

**Note:** Google Sites is a visual builder. You **cannot** simply upload the `index.html` and `style.css` files I created. You must manually rebuild the page using their editor.

1.  Go to [Google Sites](https://sites.google.com/).
2.  Start a "Blank" site.
3.  **Landing Page:**
    *   Copy the text from `play_store_assets.md` (Short Description, Features) and paste it into text boxes.
    *   Upload your app icon and screenshots using the "Images" tool.
    *   Add a button widget linking to your Play Store URL.
4.  **Privacy Policy:**
    *   Create a new page called "Privacy Policy".
    *   Copy the text from `privacy.html` (open it in a browser and copy the text) and paste it into the page.
5.  Click **Publish**.

# How to Edit This Website

Since these are standard files, you can edit them easily:

1.  **Change Text:** Open `index.html` or `privacy.html` in any text editor (like Notepad or VS Code). looking for the text you want to change (in white) and type over it.
    *   *Example:* Change `<h1>WorkScribe</h1>` to `<h1>My New App Name</h1>`.
2.  **Change Colors:** Open `style.css`. At the very top, you will see a list of colors under `:root`. Change the hex codes (e.g., `#6750A4`) to whatever color you like.
3.  **Add Images:** Put your image file (e.g., `screenshot.png`) in the `website` folder, then use `<img src="screenshot.png">` in the HTML.

## Next Steps
*   Replace the placeholder "Get it on Google Play" link in `index.html` with your actual Play Store URL once published.
*   Update the support email in `privacy.html`.
