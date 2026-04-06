# Doneski

A family chore tracker app built with vanilla JS and Firebase.

## Setup

### 1. Clone the repo

```bash
git clone https://github.com/afenrick86/doneski.git
cd doneski
```

### 2. Create your Firebase project

1. Go to [Firebase Console](https://console.firebase.google.com/) and create a new project
2. Enable **Firestore Database**, **Storage**, and **Authentication** (anonymous sign-in)
3. Go to **Project Settings → Your apps → SDK setup and configuration** and copy your config values

### 3. Configure Firebase

```bash
cp firebase.config.example.js firebase.config.js
```

Open `firebase.config.js` and replace the placeholder values with your own Firebase project config.

### 4. Run locally

Open `index.html` with a local server. The easiest option is the [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension in VS Code — right-click `index.html` and choose **Open with Live Server**.

> `firebase.config.js` is gitignored and will never be committed.

## Deploying to GitHub Pages

1. Add your Firebase config values as repository secrets (**Settings → Secrets and variables → Actions**):
   - `FIREBASE_API_KEY`
   - `FIREBASE_AUTH_DOMAIN`
   - `FIREBASE_PROJECT_ID`
   - `FIREBASE_STORAGE_BUCKET`
   - `FIREBASE_MESSAGING_SENDER_ID`
   - `FIREBASE_APP_ID`

2. Go to **Settings → Pages** and set Source to **GitHub Actions**

3. Push to `main` — the workflow in `.github/workflows/deploy.yml` will inject your config and deploy automatically
