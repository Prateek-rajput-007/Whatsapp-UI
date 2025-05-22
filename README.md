# WhatsApp Web UI Clone

A pixel-perfect WhatsApp Web clone built with **Next.js**, **Tailwind CSS**, **TypeScript**, and **Supabase**. This take-home assignment demonstrates real-time messaging, responsive design, and a clean UI consistent with WhatsApp’s design system.

![light-chat](https://user-images.githubusercontent.com/44744039/224526453-7b835f09-e25e-4bdf-894f-c1b253a8c31d.png)

## 🔗 Live Demo

> [Demo](https://whatsapp-two-beige.vercel.app/)

---

## 📌 Features

* ⚡ **Real-time Chat** using Supabase subscriptions
* 💬 Send and receive messages between users
* 🔐 User Authentication (Login UI included)
* 🎯 Pixel-perfect UI based on WhatsApp Web
* 🌗 Dark & Light Mode Support
* 🧩 Modular & Reusable Components
* 🪄 Fully Responsive using Tailwind CSS
* 🚀 Powered by TypeScript, Supabase, and Next.js

---

## 📷 Screenshots

| Login                                                                                                           | Dark Mode                                                                                                         | Chat Interface                                                                                                       | Profile                                                                                                                 |
| --------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| ![entry](https://user-images.githubusercontent.com/44744039/224526394-642e3187-57c7-47e2-995e-3f67fa52eeea.png) | ![dark-ui](https://user-images.githubusercontent.com/44744039/224526440-b4eb6a54-4dda-430c-a681-286f5b406fe7.png) | ![light-chat](https://user-images.githubusercontent.com/44744039/224526453-7b835f09-e25e-4bdf-894f-c1b253a8c31d.png) | ![light-profile](https://user-images.githubusercontent.com/44744039/224526456-40c82430-70cb-44e3-82ac-182efde8255f.png) |

---

## 🛠️ Tech Stack

* **Frontend**: Next.js, Tailwind CSS, TypeScript, React Icons
* **Backend / DB**: Supabase (PostgreSQL & Auth)
* **Realtime**: Supabase Realtime Subscriptions
* **State Management**: React Context API
* **UI/UX**: Fully responsive and accessible

---

## ✅ Mandatory Functionalities

* [x] Login UI (Styled, Functional with Supabase Auth)
* [x] Display chat list and chat window layout
* [x] Send and view messages in real-time
* [x] Messages saved and fetched from Supabase DB
* [x] Clicking a chat opens the specific conversation

---

## 🌟 Optional Features (Completed)

* [x] Filters and Search for Chats
* [x] Label chats for easier management
* [x] Assign members to different chats

---

## 💎 Bonus Features (If Implemented)

* [ ] Group Chat Support
* [ ] Sending Media Attachments
* [ ] Offline Storage via IndexedDB
* [ ] Semantic HTML tags (ongoing)

---

## 🧱 Database Schema (Supabase)

### Tables

#### `users`

| Column      | Type      | Description                |
| ----------- | --------- | -------------------------- |
| id          | UUID (PK) | Supabase Auth User ID      |
| name        | Text      | User’s display name        |
| email       | Text      | User’s email address       |
| avatar\_url | Text      | Profile picture URL        |
| created\_at | Timestamp | Timestamp of user creation |

#### `chats`

| Column      | Type      | Description                 |
| ----------- | --------- | --------------------------- |
| id          | UUID (PK) | Chat room ID                |
| name        | Text      | Chat name (optional)        |
| is\_group   | Boolean   | If the chat is a group chat |
| created\_at | Timestamp | Creation timestamp          |

#### `messages`

| Column      | Type      | Description               |
| ----------- | --------- | ------------------------- |
| id          | UUID (PK) | Unique message ID         |
| chat\_id    | UUID (FK) | ID of the chat            |
| sender\_id  | UUID (FK) | ID of the message sender  |
| content     | Text      | Message content           |
| created\_at | Timestamp | Timestamp of message sent |

#### `chat_members`

| Column          | Type      | Description        |
| --------------- | --------- | ------------------ |
| id              | UUID (PK) | Entry ID           |
| chat\_id        | UUID (FK) | Related chat ID    |
| user\_id        | UUID (FK) | Member of the chat |
| assigned\_label | Text      | Optional label/tag |

---

## 📂 Project Structure

```bash
.
├── app/
│   ├── layout.tsx
│   ├── page.tsx
├── components/
│   ├── ChatSidebar.tsx
│   ├── ChatWindow.tsx
│   ├── MessageInput.tsx
│   └── Navbar.tsx
├── hooks/
│   └── useChat.ts
├── lib/
│   └── supabase.ts
├── types/
│   └── index.ts
├── utils/
│   └── helpers.ts
├── styles/
│   └── globals.css
├── public/
│   └── icons, images etc.
└── README.md
```

---

## 📦 Setup & Installation

```bash
# 1. Clone the Repository
git clone https://github.com/prateek-007/whatsapp-clone-assignment.git
cd whatsapp-clone-assignment

# 2. Install dependencies
npm install

# 3. Add environment variables
# .env.local
NEXT_PUBLIC_SUPABASE_URL=<your-url>
NEXT_PUBLIC_SUPABASE_ANON_KEY=<your-anon-key>

# 4. Start the dev server
npm run dev
```

---

## 🧪 Testing & Linting

```bash
# Run Type Checks
tsc

# Run Linter
npm run lint

# Format Code
npm run prettier
```

---

## 🤝 Contribution

Contributions are welcome! Fork the repo, make changes and submit a pull request.

---

## 🙌 Acknowledgements

* [React Icons](https://react-icons.github.io/react-icons)
* [Supabase](https://supabase.io/)
* [Tailwind CSS](https://tailwindcss.com/)
* [Next.js](https://nextjs.org/)

