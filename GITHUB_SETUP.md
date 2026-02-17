# How to Configure Your Custom Domain (workscribe.app)

Since you are hosting on GitHub Pages and want to use `workscribe.app`, follow these steps.

## Step 1: Update Your Code (I have done this)
I have already:
1.  Created a `CNAME` file with `workscribe.app` in it.
2.  Updated `index.html` with your Play Store link.

**You just need to push these changes:**
```powershell
cd e:\workscribe-web
git add .
git commit -m "Add CNAME and Play Store link"
git push
```

## Step 2: Configure Hostinger DNS
Go to your Hostinger Domain Dashboard for `workscribe.app` and find the **DNS / Nameservers** section.

**Delete any existing A or CNAME records that might conflict (like parking pages).**

Then, add these **5 records**:

### 1. A Records (Point to GitHub)
Add these 4 separate A records. They all point `@` to GitHub's servers.

| Type | Name | Points to | TTL |
| :--- | :--- | :--- | :--- |
| A | @ | 185.199.108.153 | 3600 |
| A | @ | 185.199.109.153 | 3600 |
| A | @ | 185.199.110.153 | 3600 |
| A | @ | 185.199.111.153 | 3600 |

### 2. CNAME Record (For 'www')
This ensures `www.workscribe.app` also works.

| Type | Name | Points to | TTL |
| :--- | :--- | :--- | :--- |
| CNAME | www | workscribe.app | 3600 |

## Step 3: Verify in GitHub
1.  Go to your GitHub Repository > **Settings** > **Pages**.
2.  Under **Custom domain**, you should see `workscribe.app`.
3.  It might say "DNS check in progress". Wait 15-30 minutes.
4.  Once green, check the box **"Enforce HTTPS"** to make your site secure.

Your site will be live at `https://workscribe.app`.
