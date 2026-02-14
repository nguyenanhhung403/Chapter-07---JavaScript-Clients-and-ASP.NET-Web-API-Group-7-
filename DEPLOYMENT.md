# Vercel Deployment Guide

## 🚀 Deploy to Vercel (3 Methods)

### Method 1: Deploy via Vercel Website (Easiest!) 🌟

1. **Go to [Vercel](https://vercel.com)**
   - Login with GitHub account

2. **Click "Add New Project"**

3. **Import your GitHub repository**
   - Select: `Chapter-07---JavaScript-Clients-and-ASPNET-Web-API-Group-7-`

4. **Configure Project**
   ```
   Framework Preset: Other
   Root Directory: ./
   Build Command: npm run build
   Output Directory: src
   Install Command: npm install
   ```

5. **Click "Deploy"** 🎉

Your site will be live at: `https://your-project-name.vercel.app`

---

### Method 2: Deploy via Vercel CLI

1. **Install Vercel CLI**
   ```bash
   npm install -g vercel
   ```

2. **Login to Vercel**
   ```bash
   vercel login
   ```

3. **Deploy**
   ```bash
   vercel
   ```
   
   Follow the prompts:
   - Set up and deploy? `Y`
   - Which scope? Choose your account
   - Link to existing project? `N`
   - What's your project's name? `aspnet-architecture-docs`
   - In which directory is your code located? `./`

4. **For Production Deploy**
   ```bash
   vercel --prod
   ```

---

### Method 3: Auto-Deploy via GitHub (Recommended for Continuous Deployment)

1. **Import on Vercel** (same as Method 1)

2. **Auto-deploy on push**
   - Every `git push` to main branch = automatic deployment
   - Preview deployments for pull requests

---

## 🔧 Configuration Files

### `vercel.json`
Already created! This configures:
- Build command
- Output directory
- Caching headers
- Rewrites for proper routing

### `package.json`
Updated with:
- `npm run build` - Production build (minified CSS)
- `npm run dev` - Development with watch mode

---

## 🌐 After Deployment

Your documentation will be available at:
- **Production**: `https://your-project.vercel.app`
- **Custom Domain**: Can add in Vercel dashboard (Settings → Domains)

### View Deployment
- All deployments: `vercel ls`
- Open in browser: `vercel open`

---

## ✅ Pre-Deploy Checklist

- [x] `vercel.json` configured
- [x] `package.json` has build script
- [x] `.gitignore` includes `node_modules/`
- [x] Code pushed to GitHub
- [ ] Ready to deploy!

---

## 📱 Features After Deploy

✨ Your deployed site will have:
- **Fast CDN**: Global edge network
- **HTTPS**: Automatic SSL certificates
- **GitHub Integration**: Auto-deploy on push
- **Preview URLs**: For every commit
- **Analytics**: Built-in web analytics

---

## 🛠️ Troubleshooting

**Build fails?**
```bash
# Test build locally first
npm run build
```

**Wrong directory?**
- Check `vercel.json` outputDirectory is set to `src`

**CSS not loading?**
- Make sure Tailwind build completed
- Check `src/output.css` exists

---

## 🎯 Next Steps

1. Deploy to Vercel
2. Get your live URL
3. Share with your team
4. Set up custom domain (optional)

**Happy deploying! 🚀**
