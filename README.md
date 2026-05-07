# Remote Interview Platform

A full-stack remote technical interview platform that enables structured, real-time interviews with live code collaboration, video calls, screen sharing, and session recording — built with Next.js, TypeScript, and Convex.

🔗 **Live Demo:** [remote-interview-platform-tawny.vercel.app](https://remote-interview-platform-tawny.vercel.app)

---

## 🎯 What It Does

Running a remote technical interview has a lot of moving parts — video, code, scheduling, recording, feedback. Most teams stitch together 3–4 different tools. This platform brings it all into one place:

- Interviewers schedule and manage sessions from a dashboard
- Candidates join directly via link — no account needed
- Both sides collaborate on code in real time while on a video call
- Sessions are recorded and stored for async review

---

## ✨ Features

- 🎥 **Video calls** with screen sharing powered by Stream SDK
- 💻 **Live collaborative code editor** with real-time sync across devices
- 🗓️ **Interview scheduling & management** — create, track, and manage sessions
- 🔴 **Session recording** — replay interviews after they end
- 💬 **Real-time messaging** during live sessions via Socket.io
- 🔐 **Authentication** with Clerk — secure sign-in for interviewers
- 📊 **Candidate tracking** — persistent storage of session data and performance records
- 📱 **Mobile responsive** — works across desktop and mobile viewports

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Framework | Next.js 14 (App Router) |
| Language | TypeScript |
| Backend / DB | Convex (real-time database + serverless functions) |
| Video & Streaming | Stream SDK |
| Real-time Sync | Socket.io |
| Authentication | Clerk |
| Styling | Tailwind CSS |
| Deployment | Vercel |

---

## 📁 Project Structure

```
remote-interview-platform/
├── convex/              # Convex backend — DB schema, queries, mutations
├── public/              # Static assets
├── src/
│   ├── app/             # Next.js App Router pages
│   ├── components/      # Reusable UI components
│   ├── hooks/           # Custom React hooks
│   └── lib/             # Utility functions and config
├── next.config.mjs
├── tailwind.config.ts
└── tsconfig.json
```

---

## ⚙️ Getting Started

### Prerequisites

- Node.js v18+
- A [Convex](https://convex.dev) account
- A [Clerk](https://clerk.com) account
- A [Stream](https://getstream.io) account

### Installation

```bash
# Clone the repo
git clone https://github.com/gokulakannan18/remote-interview-platform.git
cd remote-interview-platform

# Install dependencies
npm install
```

### Environment Variables

Create a `.env.local` file in the root directory:

```env
# Convex
CONVEX_DEPLOYMENT=your_convex_deployment_url
NEXT_PUBLIC_CONVEX_URL=your_convex_public_url

# Clerk
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
CLERK_SECRET_KEY=your_clerk_secret_key
NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up

# Stream
NEXT_PUBLIC_STREAM_API_KEY=your_stream_api_key
STREAM_SECRET_KEY=your_stream_secret_key
```

### Run the App

```bash
# Start the Convex backend
npx convex dev

# In a separate terminal, start the Next.js frontend
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

---

## 🔄 How It Works

```
Interviewer creates session
        ↓
Candidate joins via link
        ↓
Video call starts (Stream SDK)
        ↓
Both edit code in real time (Socket.io sync)
        ↓
Session recorded + stored (Convex)
        ↓
Interviewer reviews recording + adds feedback
```

---

## 🚀 Deployment

The app is deployed on **Vercel** with Convex handling the backend serverless functions and real-time database.

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/gokulakannan18/remote-interview-platform)

---

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you'd like to change.

---

## 👤 Author

**K. Gokulakannan**
- GitHub: [@gokulakannan18](https://github.com/gokulakannan18)
---
