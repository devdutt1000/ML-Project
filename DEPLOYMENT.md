# Vercel Deployment Guide for ML-Project

## Prerequisites
- GitHub account with repository: https://github.com/devdutt1000/ML-Project.git
- Vercel account (sign up at https://vercel.com)

## Deployment Steps

### 1. Push Your Latest Changes to GitHub
```bash
git add .
git commit -m "Prepare for Vercel deployment"
git push origin main
```

### 2. Import Project to Vercel
1. Go to https://vercel.com/dashboard
2. Click **"Add New Project"** or **"Import Project"**
3. Select **"Import Git Repository"**
4. Choose your GitHub account and select the **ML-Project** repository
5. Click **"Import"**

### 3. Configure Project Settings
- **Framework Preset**: Other
- **Root Directory**: Leave as default (./`)
- **Build Command**: Leave empty (not needed for Flask)
- **Output Directory**: Leave empty

### 4. Environment Variables (if needed)
If your project requires any environment variables, add them in the "Environment Variables" section.

### 5. Deploy
Click **"Deploy"** button and wait for the deployment to complete (usually 2-5 minutes).

### 6. Access Your Application
Once deployed, Vercel will provide you with a URL like:
- `https://your-project-name.vercel.app`

## Important Notes

### File Structure
Your project already has the correct structure:
- ✅ `vercel.json` - Vercel configuration file
- ✅ `app.py` - Flask application entry point
- ✅ `requirements.txt` - Python dependencies
- ✅ `artifacts/` - Model files (model.pkl, preprocessor.pkl)
- ✅ `templates/` - HTML templates

### Configuration Files

**vercel.json** is already configured:
```json
{
    "builds": [
        {
            "src": "app.py",
            "use": "@vercel/python"
        }
    ],
    "routes": [
        {
            "src": "/(.*)",
            "dest": "app.py"
        }
    ]
}
```

**requirements.txt** includes all necessary dependencies:
- Flask (web framework)
- pandas, numpy (data processing)
- scikit-learn, xgboost (ML models)
- dill (model serialization)
- gunicorn (production server)

### Troubleshooting

#### If deployment fails:
1. **Check Build Logs**: In Vercel dashboard, click on your deployment and check the logs
2. **Verify Dependencies**: Ensure all packages in `requirements.txt` are compatible
3. **Check File Paths**: Make sure artifact files exist in the repository
4. **Memory Limits**: Vercel has memory limits; large models might need optimization

#### Common Issues:
- **Import Errors**: Ensure all custom modules are in the repository
- **Model Loading**: Verify `artifacts/model.pkl` and `artifacts/preprocessor.pkl` exist
- **Template Not Found**: Ensure `templates/` folder is pushed to GitHub

### Testing Locally
Before deploying, test locally:
```bash
python app.py
```
Visit: http://localhost:5000

## Continuous Deployment
Once connected to GitHub, Vercel automatically deploys:
- **Production**: Every push to `main` branch
- **Preview**: Every push to other branches or pull requests

## Alternative: Deploy via Vercel CLI

### Install Vercel CLI
```bash
npm install -g vercel
```

### Deploy
```bash
cd "d:\AIML Learning\ML-Project"
vercel
```

Follow the prompts to link your project and deploy.

## Post-Deployment

### Monitor Your Application
- View deployment logs in Vercel dashboard
- Check function execution logs
- Monitor performance and errors

### Update Your Application
To deploy changes:
```bash
git add .
git commit -m "Update message"
git push origin main
```
Vercel will automatically redeploy.

## Additional Resources
- [Vercel Python Documentation](https://vercel.com/docs/frameworks/python)
- [Vercel CLI Documentation](https://vercel.com/docs/cli)
- [Flask Deployment Guide](https://flask.palletsprojects.com/en/latest/deploying/)

---

**Your Project URL**: https://github.com/devdutt1000/ML-Project.git
**Expected Deployment URL**: `https://ml-project-[your-username].vercel.app`
