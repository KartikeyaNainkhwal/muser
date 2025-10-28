<h1 align="center">🎵 Muzer</h1>
<p align="center">
  <b>Collaborative Music Streaming Platform</b><br>
  <i>Built & maintained by <a href="https://github.com/KartikeyaNainkhwal">Kartikeya Nainkhwal</a></i>
</p>

---

## 🚀 About Muzer

**Muzer** is a modern, full-stack collaborative music streaming platform. Create spaces, share music, and enjoy real-time listening with friends. Built with Next.js, TypeScript, Prisma, WebSockets, and Docker for a seamless developer and user experience.

---

## 📋 Table of Contents

- [About Muzer](#-about-muzer)
- [Features](#-features)
- [Installation](#-installation)
  - [With Docker](#with-docker)
  - [Without Docker](#without-docker)
- [Usage](#-usage)
- [Tech Stack](#-tech-stack)
- [Contact](#-contact)
- [License](#-license)

---

## ✨ Features

- 🎶 Real-time collaborative music streaming
- 🗂️ Create and join spaces
- 👥 User authentication
- 📜 Song queue management
- ⚡ Fast, scalable, and containerized
- 🛡️ Secure with modern best practices

---

## 🛠️ Installation

### With Docker

1. **Clone the repository:**
   ```bash
   git clone https://github.com/KartikeyaNainkhwal/muser.git
   cd muzer
   ```

2. **Configure environment variables:**  
   Copy `.env.example` to `.env` in both `next-app` and `ws` folders and fill in your configuration.

3. **Start the application:**
   ```bash
   docker compose up -d
   ```

### Without Docker

1. **Clone the repository:**
   ```bash
   git clone https://github.com/KartikeyaNainkhwal/muser.git
   cd muzer
   ```

2. **Install dependencies:**
   ```bash
   cd next-app && pnpm install
   cd ../ws && pnpm install
   cd ..
   ```

3. **Configure environment variables:**  
   Copy `.env.example` to `.env` in both `next-app` and `ws` folders and fill in your configuration.

4. **Start PostgreSQL:**
   ```bash
   docker run -d \
     --name muzer-db \
     -e POSTGRES_USER=myuser \
     -e POSTGRES_PASSWORD=mypassword \
     -e POSTGRES_DB=mydatabase \
     -p 5432:5432 \
     postgres
   ```

5. **Start Redis:**
   ```bash
   docker run -d \
     --name muzer-redis \
     -e REDIS_USERNAME=admin \
     -e REDIS_PASSWORD=root \
     -e REDIS_PORT=6379 \
     -e REDIS_HOST="127.0.0.1" \
     -e REDIS_BROWSER_STACK_PORT=8001 \
     redis/redis-stack:latest
   ```

6. **Post-install scripts:**
   ```bash
   cd next-app && pnpm postinstall
   cd ../ws && pnpm postinstall
   cd ..
   ```

7. **Start the application:**
   ```bash
   cd next-app && pnpm dev
   # In a new terminal
   cd ws && pnpm dev
   ```

8. **Access Prisma Studio (optional):**
   ```bash
   cd next-app
   pnpm run prisma:studio
   ```

---

## 🌐 Usage

- App: [http://localhost:3000](http://localhost:3000)
- Redis Stack: [http://localhost:8001/redis-stack/browser](http://localhost:8001/redis-stack/browser)
- Prisma Studio: [http://localhost:5555](http://localhost:5555)

---

## 🧑‍💻 Tech Stack

- **Frontend:** Next.js, React, TypeScript, Tailwind CSS
- **Backend:** Node.js, WebSockets, Prisma, PostgreSQL, Redis
- **DevOps:** Docker, Docker Compose

---

## 📬 Contact

Maintained by [Kartikeya Nainkhwal](https://github.com/KartikeyaNainkhwal).

For questions, suggestions, or issues, please [open an issue](https://github.com/KartikeyaNainkhwal/muser/issues) or reach out via [GitHub](https://github.com/KartikeyaNainkhwal).

---

## 📝 License

This project is licensed under the MIT License.

---

<p align="center">
  <b>Made with ❤️ by Kartikeya Nainkhwal</b>
</p>
