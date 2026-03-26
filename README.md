# 🎮 GameStoreApp

A full-featured online game store built as a diploma project. The application allows users to browse, purchase, and manage games with a modern, responsive UI.

---

## 🚀 Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React 19, TypeScript, Tailwind CSS v4 |
| Build Tool | Vite |
| Backend & Auth | Firebase (Firestore, Auth, Functions, Hosting) |
| State Management | TanStack React Query |
| Payments | Stripe, PayPal |
| Forms | Formik + Yup |
| Animations | Framer Motion |
| i18n | i18next + react-i18next |
| Routing | React Router DOM v7 |
| PDF Generation | jsPDF + jspdf-autotable |
| Testing | Vitest, Playwright, Cucumber (BDD) |

---

## ✨ Features

- 🛒 Browse and purchase games
- 💳 Payment integration via **Stripe** and **PayPal**
- 🔐 User authentication via **Firebase Auth**
- 🌍 Multi-language support (i18n)
- 📄 PDF receipt / report generation
- 📱 Responsive design with Tailwind CSS
- 🔒 Google reCAPTCHA protection
- 📊 QR code generation
- 🎨 Smooth animations with Framer Motion

---

## 📁 Project Structure

```
.
├── src/                  # Application source code
├── server/               # Firebase Cloud Functions / server logic
├── public/               # Static assets
├── features/             # Cucumber BDD feature files
├── locale/               # i18n translation files
├── docs/                 # DevOps & deployment documentation
│   ├── deployment.md     # Production deployment guide
│   ├── update.md         # Update & rollback guide
│   ├── backup.md         # Backup & restore guide
│   └── scripts/          # Automation scripts
├── firebase.json         # Firebase configuration
└── vite.config.ts        # Vite configuration
```

---

## 🛠️ Developer Setup (Fresh Machine)

Follow these steps from a clean OS installation to a running development environment.

### Step 1 — Install Node.js

Download and install Node.js **v18 or higher** from https://nodejs.org (choose the LTS version).

Verify installation:
```bash
node --version   # should print v18.x.x or higher
npm --version
```

### Step 2 — Install Git

Download from https://git-scm.com and install with default settings.

Verify:
```bash
git --version
```

### Step 3 — Install Firebase CLI

```bash
npm install -g firebase-tools
firebase --version
```

### Step 4 — Clone the Repository

```bash
git clone https://github.com/klim912/Diploma.git
cd Diploma
```

### Step 5 — Install Dependencies

```bash
npm install
```

### Step 6 — Configure Environment Variables

Create a `.env` file in the root directory:

```env
VITE_FIREBASE_API_KEY=your_api_key
VITE_FIREBASE_AUTH_DOMAIN=your_project.firebaseapp.com
VITE_FIREBASE_PROJECT_ID=your_project_id
VITE_FIREBASE_STORAGE_BUCKET=your_project.appspot.com
VITE_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
VITE_FIREBASE_APP_ID=your_app_id

VITE_STRIPE_PUBLIC_KEY=pk_test_...
VITE_PAYPAL_CLIENT_ID=your_paypal_client_id
VITE_RECAPTCHA_SITE_KEY=your_recaptcha_site_key
```

> Get Firebase credentials from: https://console.firebase.google.com → Project Settings → Your apps

### Step 7 — Start Development Server

```bash
npm run dev
```

The app will open automatically at **http://localhost:5173**

---

## 📜 Available Scripts

| Command | Description |
|---|---|
| `npm run dev` | Start development server |
| `npm run build` | Build for production |
| `npm run preview` | Preview production build locally |
| `npm run lint` | Run ESLint |
| `npm run test` | Run unit tests with Vitest |
| `npm run coverage` | Run tests with coverage report |

---

## 🧪 Testing

**Unit / Component Tests** — Vitest + React Testing Library
```bash
npm run test
npm run coverage
```

**End-to-End Tests** — Playwright
```bash
npx playwright test
```

**BDD Tests** — Cucumber
```bash
npx cucumber-js
```

---

## 🚀 Deployment

See [docs/deployment.md](docs/deployment.md) for the full production deployment guide.

Quick deploy to Firebase Hosting:
```bash
npm run build
firebase deploy
```

---

## 📄 License

MIT License — see [LICENSE](LICENSE) for details.
