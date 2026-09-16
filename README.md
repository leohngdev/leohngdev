<h1 align="center">Hey, I'm Leo 👋</h1>

<p align="center">
  Software developer in <b>Melbourne, Australia</b>. I build full stack applications<br>
  end to end - schema and API layer through to the interface.
</p>

<p align="center">
  <a href="https://leohngdev.github.io"><img alt="Portfolio" src="https://img.shields.io/badge/Portfolio-leohngdev.github.io-e05561?style=for-the-badge&labelColor=0d1117"></a>
  <a href="https://www.linkedin.com/in/leo-hnguyen"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-leo--hnguyen-1f6feb?style=for-the-badge&labelColor=0d1117"></a>
  <a href="mailto:hnguyen.leo04@gmail.com"><img alt="Email" src="https://img.shields.io/badge/Email-say%20hello-3fb950?style=for-the-badge&labelColor=0d1117"></a>
</p>

---

## 🔧 Selected work

| Project | What it is | Status |
| :-- | :-- | :-- |
| **Yard** | Full stack social platform, built and deployed solo on Next.js 15, React 19 and Supabase Postgres. Authorisation lives in database row-level security rather than route checks, so no API route can return another user's records. Scheduled recommendations over embeddings and pgvector similarity. | `live` |
| **[Hospitality Till](https://github.com/leohngdev/POS)** | Point-of-sale for a restaurant: PIN auth, dine-in floor map, front-of-house tickets, kitchen chits, staff clock-in. Serves the whole venue over LAN. | `in a venue` |
| **[leohngdev.github.io](https://github.com/leohngdev/leohngdev.github.io)** | My portfolio. Astro and Tailwind, no UI framework, performance budgets enforced at build, the page measures its own weight in your browser. | `live` |
| **[ANTSA Scoring Engine](https://leohngdev.github.io/work/antsa-scoring-engine/)** | Made questionnaire scoring configurable at runtime on a production health platform: custom categories, severity thresholds, weighted scoring; and carried it through to the clinician dashboard and PDF export. | `client work` |
| **[PostMint](https://github.com/leohngdev/PostMint)** | Turns a plain-text market take into platform-formatted posts or a narrated vertical video, through a queue-backed async pipeline. | `paused` |

## 🧰 Toolkit

**Frontend**<br>
![React](https://img.shields.io/badge/React-1b1f23?style=for-the-badge&logo=react&logoColor=61dafb)
![Next.js](https://img.shields.io/badge/Next.js-1b1f23?style=for-the-badge&logo=nextdotjs&logoColor=ffffff)
![React Native](https://img.shields.io/badge/React%20Native-1b1f23?style=for-the-badge&logo=react&logoColor=61dafb)
![Tailwind](https://img.shields.io/badge/Tailwind-1b1f23?style=for-the-badge&logo=tailwindcss&logoColor=06b6d4)
![Astro](https://img.shields.io/badge/Astro-1b1f23?style=for-the-badge&logo=astro&logoColor=bc52ee)

**Backend & data**<br>
![Node.js](https://img.shields.io/badge/Node.js-1b1f23?style=for-the-badge&logo=nodedotjs&logoColor=5fa04e)
![NestJS](https://img.shields.io/badge/NestJS-1b1f23?style=for-the-badge&logo=nestjs&logoColor=e0234e)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-1b1f23?style=for-the-badge&logo=postgresql&logoColor=4169e1)
![Supabase](https://img.shields.io/badge/Supabase-1b1f23?style=for-the-badge&logo=supabase&logoColor=3fcf8e)
![MySQL](https://img.shields.io/badge/MySQL-1b1f23?style=for-the-badge&logo=mysql&logoColor=4479a1)
![Docker](https://img.shields.io/badge/Docker-1b1f23?style=for-the-badge&logo=docker&logoColor=2496ed)

**Languages**<br>
![TypeScript](https://img.shields.io/badge/TypeScript-1b1f23?style=for-the-badge&logo=typescript&logoColor=3178c6)
![JavaScript](https://img.shields.io/badge/JavaScript-1b1f23?style=for-the-badge&logo=javascript&logoColor=f7df1e)
![C#](https://img.shields.io/badge/C%23-1b1f23?style=for-the-badge&logo=dotnet&logoColor=512bd4)
![Python](https://img.shields.io/badge/Python-1b1f23?style=for-the-badge&logo=python&logoColor=3776ab)
![Java](https://img.shields.io/badge/Java-1b1f23?style=for-the-badge&logo=openjdk&logoColor=ffffff)
![C++](https://img.shields.io/badge/C%2B%2B-1b1f23?style=for-the-badge&logo=cplusplus&logoColor=00599c)
![PHP](https://img.shields.io/badge/PHP-1b1f23?style=for-the-badge&logo=php&logoColor=777bb4)

**Engines & 3D** <sub>coursework</sub><br>
![Unreal](https://img.shields.io/badge/Unreal-1b1f23?style=for-the-badge&logo=unrealengine&logoColor=ffffff)
![Unity](https://img.shields.io/badge/Unity-1b1f23?style=for-the-badge&logo=unity&logoColor=ffffff)
![Maya](https://img.shields.io/badge/Maya-1b1f23?style=for-the-badge&logo=autodeskmaya&logoColor=37a5cc)

## 🧠 How I build

<details>
<summary><b>Authorisation belongs in the database</b></summary>

<br>

An application-level permission check can be bypassed by a bug in any single route. On Yard I moved authorisation into row-level security policies inside Postgres, so no API route can return another user's records regardless of what the client asks for. Authentication runs through Google OAuth and magic link on top of that.

</details>

<details>
<summary><b>The bugs worth finding don't crash</b></summary>

<br>

The defect I am proudest of catching raised nothing at all, no error, no log entry, nothing on fire. A data mismatch had been quietly serving incorrect answer options in a production mobile app, because only the data was wrong. Anything that throws will find you on its own; the silent ones you have to go looking for.

</details>

<details>
<summary><b>Stand the environment up before writing a feature</b></summary>

<br>

I joined a project whose multiservice development environment nobody on the team could run, with no documentation to work from. I rebuilt it from scratch across service configuration, networking and dependencies before touching a ticket, which restored local development for everyone else and meant I shipped inside the first sprint.

</details>

<details>
<summary><b>Make it fail predictably</b></summary>

<br>

The first version of Yard's recommendation pipeline ranked confidently on sparse data and produced meaningless results. Confident nonsense is worse than an obvious blank. Distance thresholds and a deterministic fallback made it reliable enough to run unattended on a schedule.

</details>

---

<p align="center">
  <a href="mailto:hnguyen.leo04@gmail.com">hnguyen.leo04@gmail.com</a> · <a href="https://leohngdev.github.io">leohngdev.github.io</a>
</p>
