
## ⚙️ Setup Instructions

1. **Install Node.js & npm**
   ```bash
   node -v
   npm -v
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Run locally**
   ```bash
   npm run dev
   ```

4. **Build for production**
   ```bash
   npm run build
   ```

---

## ☁️ Deploy to Azure Static Web Apps

### Step 1: Push to GitHub

```bash
git init
git remote add origin https://github.com/<your-username>/<repo-name>.git
git add .
git commit -m "Initial commit"
git push -u origin main
```

---

### Step 2: Create Static Web App on Azure

Go to the [Azure Portal](https://portal.azure.com) and follow these steps:

####  Search for "Static Web Apps"
![image](https://github.com/user-attachments/assets/713d4565-542e-4506-b973-ec5e7c82583f)

#### 🖼️ Screenshot 2: Click "Create" and Fill in App Details
![Create Static Web App](screenshots/2-create-static-web-app.png)

#### 🖼️ Screenshot 3: Connect to GitHub Repository
![GitHub Connection](screenshots/3-github-connect.png)

#### 🖼️ Screenshot 4: Configure Build Settings
- App location: `/`
- Output location: `dist`

![Build Settings](screenshots/4-build-settings.png)

---

### Step 3: Monitor GitHub Actions

Azure sets up a workflow that builds and deploys your app. Check the **Actions** tab in GitHub to see it running:

#### 🖼️ Screenshot 5: GitHub Actions Deployment
![GitHub Actions](screenshots/5-github-actions.png)

---

## 🛠 GitHub Actions Workflow

The file `.github/workflows/azure-static-web-app.yml` handles:
- Installing dependencies
- Building the project
- Deploying to Azure Static Web Apps

#### ➕ Add this secret in GitHub:
- Go to your repo → Settings → Secrets → Actions
- Add: `AZURE_STATIC_WEB_APPS_API_TOKEN`

---

## 📦 Technology Stack

- ⚛️ **React 18**
- ⚡ **Vite**
- ☁️ **Azure Static Web Apps**
- 🔁 **GitHub Actions**

---

## 🌐 Custom Domain Setup (Optional)

1. Go to your Static Web App in Azure
2. Click on **"Custom domains"**
3. Add your domain and update your DNS records accordingly

#### 🖼️ Screenshot 6: Add Custom Domain
![Custom Domain](screenshots/6-custom-domain.png)

---

## 📄 License

This project is open-source and free to use under the [MIT License](LICENSE).

---

## 🙌 Acknowledgments

Thanks to Microsoft Azure and GitHub for enabling free and simple CI/CD deployments.
```

---

📸 **To complete the README:**
1. Create a folder called `screenshots/` in your GitHub repo.
2. Add the actual screenshots with matching names (`1-search-static-web-apps.png`, etc.).
3. GitHub will render the images automatically.

Would you like help generating or taking any of these screenshots manually or via automation?
