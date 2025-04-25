# azure-static-web-app
This is a simple React app built with **Vite** and deployed using **Azure Static Web Apps** and **GitHub Actions**.
Sure! Here's a full `README.md` file for your **Azure Static Web App** GitHub repository, including setup instructions, folder structure, and deployment info using GitHub Actions:

---

```md
# 🚀 Azure Static Web App

This is a simple React app built with **Vite** and deployed using **Azure Static Web Apps** and **GitHub Actions**.

---

## 📁 Project Structure

```
azure-static-web-app/
├── .github/
│   └── workflows/
│       └── azure-static-web-app.yml   # GitHub Actions workflow for Azure deployment
├── public/
│   └── favicon.ico                    # App icon
├── src/
│   ├── App.jsx                        # Main component
│   └── main.jsx                       # ReactDOM root
├── index.html                         # Entry HTML file
├── package.json                       # Project config and scripts
├── vite.config.js                     # Vite configuration
├── README.md                          # This file
```

---

## ⚙️ Setup Instructions

1. **Install Node.js & npm** (if not already installed)
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

### Step 2: Create a Static Web App in Azure

1. Go to the [Azure Portal](https://portal.azure.com)
2. Search for **Static Web Apps**
3. Click **Create** and fill in:
   - **GitHub Repository**: Select the repo you just pushed
   - **App location**: `/`
   - **Output location**: `dist`
4. Azure will automatically configure GitHub Actions to deploy your app on push

---

## 🛠 GitHub Actions Workflow

The file `.github/workflows/azure-static-web-app.yml` handles:
- Installing dependencies
- Building the project
- Deploying to Azure Static Web Apps using a secret token

### Add this secret in GitHub:

- Go to your repo → Settings → Secrets → Actions
- Add: `Your API Token`

---

## 📦 Technology Stack

- ⚛️ **React 18**
- ⚡ **Vite** for fast builds
- ☁️ **Azure Static Web Apps**
- 🔁 **GitHub Actions** for CI/CD

---

## 📄 License

This project is open-source and free to use under the [MIT License](LICENSE).
