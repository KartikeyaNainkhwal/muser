<h1 align="center">🎵 Muzer</h1>
<p align="center">
  <b>Collaborative Music Streaming Platform</b><br>
  <i>Built & maintained by <a href="https://github.com/KartikeyaNainkhwal">Kartikeya Nainkhwal</a></i>
</p>

---

## 📋 Table of Contents

- [Installation](#installation)
  - [With Docker](#with-docker)
  - [Without Docker](#without-docker)
- [Usage](#usage)
- [Contact](#contact)

---

## 🛠️ Installation

### With Docker

1. **Clone the repository:**
   ```bash
   git clone https://github.com/KartikeyaNainkhwal/muser.git
   cd muzer/next-app
   ```
2. **(Optional)** Create a Docker volume if you face mount/volume errors:
   ```bash
   docker volume create postgres-data
   ```
3. **Start the application:**
   ```bash
   docker-compose up -d
   ```

### Without Docker

1. **Clone the repository:**
   ```bash
   git clone https://github.com/KartikeyaNainkhwal/muser.git
   cd muzer/next-app
   ```
2. **(Optional) Start a PostgreSQL database using Docker:**
   ```bash
   docker run -d \
     --name muzer-db \
     -e POSTGRES_USER=myuser \
     -e POSTGRES_PASSWORD=mypassword \
     -e POSTGRES_DB=mydatabase \
     -p 5432:5432 \
     postgres
   ```
   Example connection URL:
   ```
   DATABASE_URL=postgresql://myuser:mypassword@localhost:5432/mydatabase?schema=public
   ```
3. **Create a `.env` file** based on `.env.example` and configure your `DATABASE_URL`.
4. **Install dependencies:**
   ```bash
   pnpm install
   ```
5. **Run database migrations:**
   ```bash
   pnpm run prisma:migrate
   ```
6. **Start the development server:**
   ```bash
   pnpm run dev
   ```

---

## 🌐 Usage

- Access the application in your browser at [http://localhost:3000](http://localhost:3000)

---

## 📬 Contact

Maintained by [Kartikeya Nainkhwal](https://github.com/KartikeyaNainkhwal).

For questions, suggestions, or issues, please [open an issue](https://github.com/KartikeyaNainkhwal/muzer/issues).
