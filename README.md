# ValorVault Landing Page

A modern, responsive landing page for the ValorVault Android app.

## Files Structure

```
valorvault_website/
├── index.html          # Main HTML file
├── styles.css          # CSS styles
├── script.js           # JavaScript functionality
├── assets/
│   ├── logo.png        # App logo
│   ├── vaults.png      # Valors/coins icon
│   ├── app-screenshot.png  # (You need to add this)
│   └── valorvault.apk  # (You need to add your APK here)
└── README.md           # This file
```

## How to Add Your APK for Download

### Step 1: Build Your APK
1. In Android Studio, go to **Build > Build Bundle(s) / APK(s) > Build APK(s)**
2. Wait for the build to complete
3. Click **"locate"** in the notification, or find it at:
   ```
   app/build/outputs/apk/debug/app-debug.apk
   ```
   Or for release:
   ```
   app/build/outputs/apk/release/app-release.apk
   ```

### Step 2: Copy APK to Website
1. Rename your APK to `valorvault.apk`
2. Copy it to the `assets` folder:
   ```
   valorvault_website/assets/valorvault.apk
   ```

### Step 3: Update Version Info (Optional)
In `index.html`, find this line and update the version:
```html
<span class="btn-subtitle">Version 1.0.0 • Android 7.0+</span>
```

## How to Add App Screenshot

1. Take a screenshot of your app (preferably the home screen)
2. Save it as `app-screenshot.png`
3. Place it in the `assets` folder
4. Recommended size: 1080x1920 pixels (portrait)

## Hosting Options

### Option 1: GitHub Pages (Free)
1. Create a new GitHub repository
2. Upload all website files
3. Go to **Settings > Pages**
4. Select **main** branch and **/ (root)**
5. Your site will be live at: `https://yourusername.github.io/repository-name`

### Option 2: Netlify (Free)
1. Go to [netlify.com](https://netlify.com)
2. Sign up with GitHub
3. Click **"Add new site" > "Import an existing project"**
4. Select your repository
5. Deploy!

### Option 3: Vercel (Free)
1. Go to [vercel.com](https://vercel.com)
2. Sign up with GitHub
3. Import your repository
4. Deploy automatically

### Option 4: Firebase Hosting (Free)
1. Install Firebase CLI: `npm install -g firebase-tools`
2. Login: `firebase login`
3. Initialize: `firebase init hosting`
4. Deploy: `firebase deploy`

## Customization

### Change Colors
Edit the CSS variables in `styles.css`:
```css
:root {
    --primary: #FFD700;       /* Main gold color */
    --primary-dark: #B8860B;  /* Darker gold */
    --secondary: #FFA500;     /* Orange accent */
    --background: #0a0a0f;    /* Dark background */
}
```

### Update Statistics
In `index.html`, find the hero stats section:
```html
<div class="hero-stats">
    <div class="stat">
        <span class="stat-number">10K+</span>
        <span class="stat-label">Active Users</span>
    </div>
    ...
</div>
```

### Add Social Links
Update the footer social links with your actual URLs:
```html
<div class="social-links">
    <a href="YOUR_FACEBOOK_URL"><i class="fab fa-facebook-f"></i></a>
    <a href="YOUR_TWITTER_URL"><i class="fab fa-twitter"></i></a>
    ...
</div>
```

## Testing Locally

### Method 1: Direct Open
Just double-click `index.html` to open in your browser.

### Method 2: Live Server (Recommended)
1. Install VS Code extension "Live Server"
2. Right-click `index.html` > "Open with Live Server"
3. Auto-refreshes when you make changes!

### Method 3: Python Simple Server
```bash
cd valorvault_website
python -m http.server 8000
```
Then open: http://localhost:8000

## Notes

- The APK download will only work when hosted on a server (not when opening HTML directly)
- Make sure your APK is named exactly `valorvault.apk` or update the href in index.html
- Large APK files (>25MB) may need to be hosted elsewhere (like Google Drive)

## APK Hosting Alternatives (for large files)

If your APK is too large for your hosting:

### Google Drive
1. Upload APK to Google Drive
2. Right-click > "Get link" > "Anyone with the link"
3. Copy the link
4. Convert to direct download link:
   - Original: `https://drive.google.com/file/d/FILE_ID/view?usp=sharing`
   - Direct: `https://drive.google.com/uc?export=download&id=FILE_ID`
5. Update the download button href in index.html

### Dropbox
1. Upload APK to Dropbox
2. Get shareable link
3. Change `?dl=0` to `?dl=1` for direct download

---

Made with ❤️ for ValorVault
