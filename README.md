# Shak Code 🚀

**Shak Code** is an interactive coding-learning web app designed to help learners study programming, practise writing code, and track their progress in one place.

## ✨ Features

- **Learn:** Structured lessons for **C, C++, Python, and Java**.
- **Practice:** An in-app code editor for writing and running programs.
- **Code execution:** Uses a Judge0-based execution flow through the app's backend.
- **Jarvis Tutor:** An AI learning assistant for programming questions and explanations.
- **Fix My Code:** Get help understanding and correcting code errors.
- **Challenges:** Practise concepts with coding challenges and earn progress/XP.
- **Mastery checks:** Test understanding of lesson topics.
- **Progress and profile:** Keep track of learning progress and account details.
- **Responsive interface:** Includes mobile-friendly navigation.
- **Authentication and data:** Uses Supabase for backend services and app data.

## 🧰 Tech Stack

| Technology | Purpose |
|---|---|
| HTML, CSS, JavaScript | Frontend and interactive user interface |
| Supabase | Backend services, authentication, database, and Edge Functions |
| Gemini API | AI-powered Jarvis Tutor responses (configured on the backend) |
| Judge0 | Running submitted code in supported programming languages |
| Cloudflare | Hosting/deployment for the web app |
| Git and GitHub | Version control and source-code hosting |

> The exact services and configuration may vary with the current deployment. Keep API keys and other secrets in backend environment/secrets settings—never commit them to this repository.

## 🏗️ How It Works

1. A learner opens Shak Code in a browser.
2. The frontend communicates with Supabase for supported account, data, and AI features.
3. Jarvis Tutor requests are handled by the backend, which uses the configured Gemini model/fallback setup.
4. Code submissions are sent through the backend's `run-code` flow to the Judge0 execution service.
5. The app displays results and updates learning progress where applicable.

## 🚀 Getting Started

### 1. Get the source code

Clone your GitHub repository, then open the project folder:

```bash
git clone <YOUR_REPOSITORY_URL>
cd <YOUR_REPOSITORY_FOLDER>
```

Replace the placeholders with your actual repository URL and folder name.

### 2. Open the frontend

Open the project's main HTML entry point (for example, `index.html`) in a browser or use a local development server. If your repository uses a different entry point or build setup, follow that project's structure.

### 3. Configure backend services

To use backend-dependent features, configure the existing Supabase project and Edge Functions. Set required credentials and service URLs in the appropriate frontend configuration or backend secrets, according to the current implementation.

- Configure Gemini credentials on the backend for Jarvis Tutor.
- Configure the Judge0 endpoint/API credentials used by `run-code`.
- Ensure Supabase authentication, database policies, and Edge Functions are deployed and configured.

**Never place private API keys, service-role keys, or other secrets in frontend code or commit them to GitHub.** Public client configuration should only be used as intended by Supabase, with Row Level Security (RLS) and appropriate policies enabled.

## 🌐 Deployment

Shak Code's frontend is deployed through Cloudflare. For updates to a Git-connected deployment:

1. Edit and test the files locally.
2. Review the changes:
   ```bash
   git status
   git diff
   ```
3. Commit the update:
   ```bash
   git add .
   git commit -m "Describe your update"
   ```
4. Push to the branch connected to Cloudflare:
   ```bash
   git push
   ```
5. Wait for the Cloudflare build/deployment to finish, then test the live site.

If the Cloudflare project is not connected to the repository, use the deployment method configured for that project instead.

## 🔐 Security Notes

- Do not commit `.env` files, API keys, access tokens, or Supabase service-role credentials.
- Keep privileged operations in backend Edge Functions.
- Apply and test Supabase Row Level Security policies for tables containing user data.
- Validate code-execution requests on the backend and enforce appropriate execution limits.

## 🧪 Testing Checklist

Before publishing an update, test:

- Sign up, sign in, and sign out.
- Lesson navigation, lesson questions, and mastery-check retry behavior.
- Code execution for each supported language, including programs that request input.
- Jarvis Tutor and Fix My Code responses.
- Challenge answer checking and progress/XP updates.
- Mobile navigation and layouts.
- Backend-unavailable/error messages.

## 🤝 Contributing

This is a learning project. To propose a change, create a branch, make a focused update, test it, and open a pull request or share the change with the project maintainers.

## 📄 License

No license has been specified yet. Unless a license is added to this repository, reuse and redistribution are not automatically permitted.

---

Built as a project to make learning programming more interactive and approachable. 💻
