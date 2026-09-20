# NoteHub Application (With Authentication & SSR)

Full-stack web application for managing personal notes with cookie-based user authentication,
SSR/CSR integration, route protection, user profile management, and global state synchronization
using **Next.js (App Router)**, **TypeScript**, **Zustand**, **TanStack Query**, and **Axios**.

---

## 🚀 Demo & Links

- **Live Demo (Vercel):** [Live page](https://09-auth-pearl-xi.vercel.app/)
- **Repository:** [GitHub](https://github.com/SerdiukSerhii/09-auth)

---

## 🛠️ Tech Stack

- **Framework:** Next.js (App Router)
- **Language:** TypeScript
- **Asynchronous State Management:** TanStack Query (`@tanstack/react-query`)
- **Global Client State:** Zustand
- **HTTP Client:** Axios (with cookie support via `withCredentials: true`)
- **Cookie Parsing:** `cookie`
- **Styling:** CSS Modules + `modern-normalize`
- **Form Management & Debouncing:** Formik, Yup, `use-debounce`
- **Linter / Formatter:** Prettier & ESLint

---

## 📌 Features

1. **Authentication System:** Cookie-based user registration (`/sign-up`), login (`/sign-in`),
   logout, and session check endpoints.
2. **Global Auth State Synchronization:** `AuthProvider` wrapper checking session validity and
   syncing user profile data to the Zustand auth store (`lib/store/authStore.ts`).
3. **Route Protection (Proxy/Middleware):** Private route enforcement (`/notes`, `/profile`)
   preventing unauthorized access and redirecting authenticated users away from public auth pages.
4. **User Profile & Editing:** SSR user profile page (`/profile`) and client-side profile editing
   (`/profile/edit`) updating state and triggering automatic navigation.
5. **Separated API Architecture:** Modular layer distinguishing client-side requests
   (`lib/api/clientApi.ts`), server-side requests forwarding request headers/cookies
   (`lib/api/serverApi.ts`), and shared Axios instances (`lib/api/api.ts`).
6. **Note Management with Search & Pagination:** Debounced filtering, server-side note fetching,
   note creation, and note deletion.

---

## ⚙️ Local Setup and Installation

1. Clone the repository and navigate to the project folder:

   git clone https://github.com/SerdiukSerhii/09-auth

   cd 09-auth

2. Install dependencies:

   npm install

3. Create a .env file in the root directory and specify the API base URL:

   NEXT_PUBLIC_API_URL=http://localhost:3000

4. Start development mode:

   npm run dev

5. Production build:

   npm run build

---

## Author

**Serhii Serdiuk**
