# 🏍️ MotoRadar

MotoRadar is a platform that brings together essential features for motorcyclists into one application. It aims to create an active and useful community where users can share routes, events, classifieds, and request roadside assistance when needed.

---

## 🚀 Project Goal

To create a full-stack application (API + UI) that supports the motorcyclist community, enhances safety, and improves information sharing on the road.

---

## 🔗 Links

- 🎨 [Figma Design](https://www.figma.com/design/TGvAjL17XIaSoKemeAOeQO/FINAL_PROJECT?node-id=0-1&p=f&t=bNDEiI4frhEMroet-0)
- 📋 [Jira Board](https://silverreinart01-1760074771033.atlassian.net/jira/software/projects/SMS/boards/1)

---

## 🛠️ Tech Stack

### Frontend

| Technology    | Purpose                              |
|---------------|--------------------------------------|
| **Next.js**   | React framework for SSR/SSG          |
| **Tailwind CSS** | Utility-first CSS for styling     |
| **Mapbox GL JS** | Interactive maps for GPS features |

### Backend

| Technology     | Purpose                                 |
|----------------|-----------------------------------------|
| **Node.js + Express** | RESTful API                     |
| **Socket.io**   | Real-time communication (live map, SOS) |
| **PostgreSQL + PostGIS** | Spatial data & route storage  |
| **Prisma ORM** | Type-safe database access               |

### Deployment

| Layer         | Tech / Service Suggestions            |
|---------------|----------------------------------------|
| **Frontend**  | Vercel or Netlify                     |
| **Backend**   | Railway, Render, Fly.io               |
| **Database**  | Supabase (PostgreSQL + PostGIS)       |
| **Containers**| Docker (optional for local dev)       |

---

## 🔧 Core Features

### 📍 Route Tracking
- Logs GPS-based routes in real time.
- Displays distance, duration, and speed stats.
- Routes can be saved, rated, and shared.

### 🧭 Route Sharing & Categorization
- Upload and explore community-shared routes.
- Categories: Offroad, Asphalt, Mixed, etc.
- Includes photos, difficulty ratings, descriptions.

### 🆘 Emergency Assistance (SOS)
- Request roadside help with GPS location and issue description.
- Nearby riders receive real-time alerts via Socket.io.
- Map markers show active SOS requests.

### 👥 Live User Map
- Shows online users on a map (if opted in).
- Join rides or see nearby riders.
- Toggle visibility at any time.

### 📢 Info Board & Classifieds
- Post and browse events, classifieds, and motorcycle services.
- Filter posts by topic, location, or date.
- Useful for meetups, gear trades, or shop recommendations.

---

## 📅 Estimated Timeline

| Phase                          | Description                                              | Duration       |
|-------------------------------|----------------------------------------------------------|----------------|
| 📝 Planning & Specification     | Requirements, UX/UI design, tech setup                  | 2–3 weeks      |
| 🏗️ Backend Development         | REST API, database models, geolocation features         | 4–6 weeks      |
| 🎨 Frontend Development        | UI components, map integration, forms                   | 5–7 weeks      |
| 🔄 Feature Integration         | Real-time map, SOS, route sharing                       | 3–4 weeks      |
| 🧪 Testing & QA                | Manual/user testing, bug fixes, optimizations           | 2–3 weeks      |
| 🚀 Launch                     | Beta release + feedback loop                            | 2 weeks        |

> **⏱️ Total Estimated Duration: 4–5 months**

---

## 🧭 Project Structure (Monorepo Example)

