# 🤖 SahayakAi

**AI-Powered Customer Support Platform with Embeddable Chat Widget**

SahayakAi is a modern, full-stack SaaS application that enables businesses to deploy intelligent AI chatbots on any website with a single line of code. Built with Next.js 16, Google Gemini AI, and enterprise-grade authentication.

---

## ✨ Features

- 🚀 **Embeddable Chat Widget** - Drop-in JavaScript widget for any website
- 🤖 **AI-Powered Responses** - Google Gemini AI integration for intelligent conversations
- 🔐 **Enterprise SSO Authentication** - Scalekit integration for secure user management
- 📊 **Dashboard** - Manage settings, view analytics, and customize your chatbot
- 🎨 **Beautiful UI** - Modern, responsive design with Tailwind CSS and Framer Motion
- 💾 **MongoDB Database** - Scalable data persistence
- ⚡ **Real-time Chat** - Fast, seamless customer interactions
- 🔧 **Customizable** - Configure chatbot behavior per user/organization

---

## 🛠️ Tech Stack

**Frontend:**
- Next.js 16 (App Router)
- React 19
- TypeScript
- Tailwind CSS 4
- Framer Motion

**Backend:**
- Next.js API Routes
- MongoDB with Mongoose
- Google Gemini AI (@google/genai)

**Authentication:**
- Scalekit SDK (SSO/SAML)

---

## 📦 Installation

### Prerequisites
- Node.js 20+ 
- MongoDB database
- Google Gemini API key
- Scalekit account (for SSO)

### Setup

1. **Clone the repository**
```bash
git clone <repository-url>
cd SahayakAi
```

2. **Install dependencies**
```bash
npm install
```

3. **Configure environment variables**

Create a `.env.local` file in the root directory:

```env
# MongoDB
MONGODB_URI=your_mongodb_connection_string

# Google Gemini AI
GEMINI_API_KEY=your_gemini_api_key

# Scalekit SSO
SCALEKIT_ENV_URL=your_scalekit_env_url
SCALEKIT_CLIENT_ID=your_client_id
SCALEKIT_CLIENT_SECRET=your_client_secret

# Next.js
NEXT_PUBLIC_APP_URL=http://localhost:3000
```

4. **Run the development server**
```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

---

## 🚀 Usage

### For Platform Users

1. **Sign In** - Authenticate via SSO
2. **Access Dashboard** - Navigate to `/dashboard` to manage your chatbot
3. **Configure Settings** - Customize AI behavior, branding, and responses
4. **Get Embed Code** - Copy your unique embed script
5. **Deploy Widget** - Add the script to any website

### Embedding the Chatbot

Add this script tag to any HTML page:

```html
<script 
  src="https://your-domain.com/chatBot.js" 
  data-owner-id="YOUR_UNIQUE_OWNER_ID"
></script>
```

The chatbot will automatically appear as a floating widget in the bottom-right corner.

---

## 📡 API Routes

| Route | Method | Description |
|-------|--------|-------------|
| `/api/auth/login` | GET | Initiate SSO login flow |
| `/api/auth/callback` | GET | Handle SSO callback |
| `/api/auth/logout` | GET | End user session |
| `/api/chat` | POST | Process chat messages with AI |
| `/api/settings` | POST | Update chatbot settings |
| `/api/settings/get` | GET | Retrieve chatbot settings |

---

## 📂 Project Structure

```
SahayakAi/
├── public/
│   └── chatBot.js          # Embeddable widget script
├── src/
│   ├── app/
│   │   ├── api/            # API routes
│   │   ├── dashboard/      # Dashboard page
│   │   ├── embed/          # Embed demo page
│   │   └── page.tsx        # Home page
│   ├── components/         # React components
│   ├── lib/                # Utilities (DB, auth, etc.)
│   └── model/              # MongoDB schemas
├── .env.local              # Environment variables
└── package.json
```

---

## 🎨 Key Components

### ChatBot Widget (`public/chatBot.js`)
Lightweight, vanilla JavaScript widget that:
- Creates floating chat button
- Renders chat interface
- Communicates with SahayakAi API
- Zero dependencies, works anywhere

### Dashboard (`/dashboard`)
User management interface for:
- Viewing embed code
- Configuring AI settings
- Managing organization settings

### Chat API (`/api/chat`)
Handles incoming messages:
- Validates owner ID
- Fetches user settings from MongoDB
- Generates AI responses via Google Gemini
- Returns formatted replies

---

## 🔒 Authentication Flow

1. User clicks "Login"
2. Redirected to Scalekit SSO
3. SSO provider authenticates user
4. Callback returns user to `/api/auth/callback`
5. Session created and stored
6. User redirected to dashboard

---

## 🌐 Deployment

### Deploy on Vercel

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new)

1. Push code to GitHub
2. Import project to Vercel
3. Add environment variables
4. Deploy

### Environment Variables (Production)
Ensure all `.env.local` variables are set in your hosting platform.

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License.

---

## 🙋 Support

For questions or issues, please open an issue on GitHub or contact support.

---

**Built By Satyam Kanojiya using Next.js and Google Gemini AI**
"# SahayakAI" 
